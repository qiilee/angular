һ��������ļ̳�
    ���� html ���а�����ϵ��. ����״�ṹ.
    ����״�ṹ�к��� controller ������, ����֮��Ӧ�ľ�����״�� scope �ṹ.
    ����:
        <body ng-app="mainApp">
            <div ng-controller="controller1">
                <div ng-controller="controller3"></div>
            </div>
            <div ng-controller="controller2"></div>
        </body>
    html:
        body
            div
                div
            div
    scope Ҳ���ڸýṹ
        $rootScope
            $scope: scope1
                $scope: scope3
            $scope: scope2
    �� scope �ṹ�� ԭ�ͼ̳й�ϵ
        scope2 -> $rootScope -> Object.prototype -> null
        scope3 -> scope1 -> $rootScope -> Object.prototype -> null
    ԭ�ͼ̳и���������������ԭ��




����scope
        scope ����������. ���������۵�ʱ��˵����������ָ�����ķ��ʷ�Χ.
        �� ng �� ���е����� Ӧ���� viewmodel ��, ���� ng ��ʹ�� "ģ��" ���ֹ���.
        ����� ng �� ���ǵ� "ģ��" ����һ�������ķ�������.

        �� ng ����������һ�� ����. ��ν�� ����������, ��ָ�ڶ����пɷ��ҵ���Ӧ������.

        ʹ�� ����: ������ ��Ҫʲô����. �� scope �о��ṩʲô����.

        ��¼��֤��
            �����û���¼, ��Ҫ��֤�û�������û�, ��������ݱ�����ڷ���������ύ.
            ���Ƚ����� �������ı���, һ�����û���, һ��������
            ����һ�� ��ť�����ύ( submit )


        ��ϰ:
            1> �� ng ʵ�� ��¼��֤
            2> ʹ�� ng ʵ�� ע����֤

        ng �� DOM �¼�, ng-click="func()" ���һ��. ���뵽��ʲô?