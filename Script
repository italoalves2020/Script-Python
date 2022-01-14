import pyodbc



string_dw = ("DRIVER={SQL Server};"
             "SERVER=AQUI_NOME_DO_SERVER_DO_SEU_SQL;"
             "Database=LIVRARIA;")
conexao_dw = pyodbc.connect(string_dw)
cursor_dw = conexao_dw.cursor()
print("Conectado ao banco")

nome_Livro = input("Qual nome do livro?")
nome_Autor = input("Qual nome do autor?")
sexo_Autor = input("Qual sexo do autor?")
num_Paginas = input("Qual numero de paginas?")
nome_Editora = input("Qual nome da editora?")
vl_Livro = input("Qual valor do livro?")
uf_Editora = input("Qual uf da editora?")
ano_Publi = input("Qual ano de publicacao?")

query = '''insert into LIVROS (NomeLivro , NomeAutor , SexoAutor , NumeroPaginas , NomeEditora , ValorLivro , UFEditora , AnoPublicacao) values('''
script = query + '\'' + str(nome_Livro) + '\',\'' + str(nome_Autor) + '\',\'' + str(sexo_Autor) + '\',' + str(int(num_Paginas)) + ',\'' + str(nome_Editora) + '\',' + str(float(vl_Livro)) + ',\'' + str(uf_Editora) + '\',' + str(int(ano_Publi)) + ''')'''
cursor_dw.execute(script)
cursor_dw.commit()
cursor_dw.close()
print('Dados Inseridos')

opcao = input("Deseja alterar alguma informação? S ou N")
if opcao == 'S':
    alter = input("Digite o script para alterar?")
    res = '''UPDATE SET''' + str(alter)
    cursor_dw.execute(res)
    cursor_dw.commit()
    cursor_dw.close()
else:
    print("Programa Finalizado!!")
