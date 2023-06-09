# Flutter-rattrapage
import 'package:flutter/material.dart';

class StudentsListPage extends StatefulWidget {
  @override
  _StudentsListPageState createState() => _StudentsListPageState();
}

class _StudentsListPageState extends State<StudentsListPage> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Liste des étudiants'),
      ),
      body: Container(
        // Contenu de la liste des étudiants ici
      ),
    );
  }
}

  
  ListView.builder(
  itemCount: students.length, // Remplacez students par la liste réelle des étudiants
  itemBuilder: (context, index) {
    final student = students[index]; // Remplacez students par la liste réelle des étudiants

    return ListTile(
      title: Text('${student.nom} ${student.prenom}'),
      subtitle: Column(
        crossAxisAlignment: CrossAxisAlignment.start,
        children: [
          Text('Classe: ${student.classe}'),
          Text('Matricule: ${student.matricule}'),
          Text('Email: ${student.email}'),
        ],
      ),
    );
  },
);
