1. ��ϰ�����
    -> ��ϰ
        -> MVC �� MVVM �Ļ�������
        -> ng �Ļ���ʹ��
        -> ����ģ��
            /* var module = */ angular.module( 'mainApp', [] )
            ģ�鴴��������ȥ����?
            ���ģ��ķ���
                angular.module( 'mainApp' )
            ģ������?

            ģ��( ��һ������ʵ�� )
            (function () {
                var modules = {}; // ����
                var angular = {};

                angular.module = function ( name, requires ) {
                    var module;
                    if ( requires ) {
                        // ����ģ��
                        module = { name: name };
                        modules[ name ] = module;
                    } else {
                        module = nudules[ name ]
                    }
                    return module;
                };
            })()

        -> ��ģ��( ����� )
            ��������ģ�����˼( ���� mix )
                ������һ��ģ�� 'moduleA'
                    angular.module( 'moduleA', [] )
                        .controller( ... )
                        .filter( ... )
                        .services( ... )
                        .directive( ... )
                        ....
                    // ���һ�ºñ���һ�� ���� ���� moduleA
                    // ���кܶ������, �ֱ��� controller, filter, services, directive, ...
                ����һ��ģ�� mainApp, �� moduleA ���ؽ���
                    angular.module( 'mainApp', [ 'moduleA' ] )
                    // ���һ��. ��ʱ�ñ���һ������� mainApp.
                    // ������������˼���� �� moduleA �� "����" ���뵽 mainApp ��
            ��ģ��Э��
                �ֱ�������� �ı����˫�����ݰ�


2. �ĵ�
    1> angular �� angularjs �Ĺ�ϵ
    2> �ٷ��ĵ�
        -> ����: https://code.angularjs.org/
        -> �� ��ѹ��� js �ļ�Ŀ¼�� � http ������
        -> ���˼������һ�㶼�� ������
            ����� win7+ ���Դ��� iis ������( internet information services )
            -> �������
            -> ɾ������
            -> �򿪻�ر�win����
            -> ѡ��װ
            -> �ڹ������оͿ��Կ��� iis ������
        -> ע��: ����з���Ȩ�޵�����
            -> �Ҽ� -> ��ȫ -> �༭ -> ����û��� everyone -> �����ȫ���Ƶ�Ȩ�� -> ���漴��
        -> ����ǵ��Թ�˾װ����Ĳ���ϵͳ, ����ʹ�� apache �� http-server


3.angular.module( 'moduleA', [] ) ����һ��moduleAģ��
    .controller( ... ) ������
    .filter( ... )  ������
    .services( ... ) ����
    .directive( ... )  ָ��
    ....
    ģ���ﴴ���Ķ������������ģ��

    2����������ģ�����˼������һ��ģ���еĿ������������������ŵ���ģ����

    3���ڲ���provider����

    4��������������������ĺ���