# hwsraf
Напишите программу, которая находит среднее арифметическое всех чисел, записанных в файле в столбик, и выводит результат в другой файл
var
    fIn, fOut: text;
    sr: real;
    a, b: longint;

begin
    sr := 0;
    b := 0;
    assign(fIn, 'input.txt');
    assign(fOut, 'output.txt');
    reset(fIn);
    rewrite(fOut);
    while not eof(fIn) do
    begin
        readln(fIn, a);
        sr += a;
        b += 1;
    end;
    sr /= b;
    writeln(fOut, sr);
    close(fIn);
    close(fOut);
end.
