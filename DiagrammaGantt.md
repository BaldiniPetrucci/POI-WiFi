<!DOCTYPE html>
<html lang="en">
    <head>
        <title>App Panini</title>
        <script src="node_modules/frappe-gantt/dist/frappe-gantt.js"></script>
        <link rel="stylesheet" href="node_modules/frappe-gantt/dist/frappe-gantt.css">
        <link rel="stylesheet" href="cssAppPanini.css">
    </head>
    <body>
        <div class="cointainer">
            <div class="gantt-target">
            </div>
        </div>
        <script>//interpretato come java
            var tasks = [//array di oggetti(list)
            {
                    start: '2021-01-15',//attributo
                    end: '2021-02-01',
                    name: 'Analisi commessa',
                    id: 'task_0',
                    progress: 20,//percentuale
                },
                {//Modello E-R
                    start: '2021-02-01',
                    end: '2021-02-07',
                    name: 'Progettazione concettuale',
                    id: 'task_1',
                    progress: 0,
                    dependencies: 'task_0'
                },
                {//Modello Relazionale 
                    start: '2021-02-07',
                    end: '2021-02-13',
                    name: 'Progettazione logica',
                    id: 'task_2',
                    progress: 0,
                    dependencies: 'task_1'
                },
                {//Implementazione-Progettazione fisica
                    start: '2021-02-13',
                    end: '2021-02-19',
                    name: 'Progettazione fisica',
                    id: 'task_3',
                    progress: 0,
                    dependencies: 'task_2'
                },
                {//test
                    start: '2021-02-19',
                    end: '2021-02-25',
                    name: 'Test di Validazione e Collaudo',
                    id: 'task_4',
                    progress: 0,
                    dependencies: 'task_3'
                },
                {// manutenzione del database
                    start: '2021-02-25',
                    end: '',
                    name: 'Manutenzione',
                    id: 'task_5',
                    progress: 0,
                    dependencies: 'task_4'
                }  
            ]
            var gantt_char= new Gantt(".gantt-target", tasks,{
                view_modes:['Quarter Day','Half Day'],
                view_mode: 'Week',
                on_click: function(task){
                    console.log(task);
                    alert('ciao');
                },
            });//per vederlo           
        </script>
    </body>
</html>

