6. ���ʽ( expression )
    javascript ���ʽ
        �� js �� ��ν�ı��ʽ���� ����������������ݶ��õ�����ֵ���ַ�����.
            �������ʽ: 123, {}, function () {}, ...
                    ������( ֱ����, literal )
            �������ʽ: 123+456, 123/456, ...
            �ַ����ӱ��ʽ: '123'+456
            �������ñ��ʽ: func()
            ... ...

    angularjs ���ʽ
        �� ֵ���� �� ָ�������ڼ�����滻�� ������ js �Ĵ���Ƭ��
        ����: ng-model="txt", {{ txt }}, ng-click="func()", ...

        ��Ҫ��Ҫ���֪�����ʽ��ʲô����( ���� )

    ng ���ʽ�� js ���ʽ����ͬ( �ص� )
        1) ������( this )
            js: this �� window
                ng ֻ���� scope �ķ���������( ���������е����ݶ��� scope ������ )
            ng: this ��ָ��ǰ�� scope
        2) �ݴ���
            js: console.log( num ) ����, num δ����
            ng: {{ txt }} �� scope �м�ʹû�и�����Ҳ���ᱨ��, ֻ����Բ���ʾ
        3) ������( filter )
            js �в����� ������
            ng �к��й�����
        4) ...


    ���Ǳ��ʽ�е�����( ��ʶ�� )���� scope ������
        {{ message }}
        {{ num1 + num2 + num3 }}
        ng-style="obj"

    ng-click ��һ�� dom �¼���, ��һ��Ҫ���� ��������, Ҳ����ֱ�ӷ������.
        �京���� �ڱ�ǩ��д�� onclick="���" Ч��һ��.
        ����:
            <a href="..." onclick="console.log( '��������' ); return false;"></a>
            ����������ַ�������һ�� ��������, ������Ĵ����߼��ϵȼ���
            a.onclick = function () {
                console.log( '��������' );
                return false;
            };
        ͬ��:
            ng-click="func()"
            �߼��ϵȼ���
            $scope.??? = function () {
                $scope.func();
            }