import SimpleSchema from 'simpl-schema'

let EtudiantSchema = new SimpleSchema({
  apogee: !String,
  cne: !String,
  cin: !String,
  nom: !String,
  prenom: !String,
  dateNaiss: !Date,
  nationalité: !String,

  inscrit: {
    filiere: !String,
    semestre: ![Number],
    module: ![String]
  },
  note: {
    resultat: [
      {
        annee: String,
        ord: [
          {
            codeMod: String,
            note: Number,
            isVal: Boolean
          }
        ],
        Rat: [
          {
            codeMod: String,
            note: Number,
            isVal: Boolean
          }
        ]
      }
    ],
    archive: {
      L1: {
        isVal: Boolean,
        mention: String,
        S1: {
          isVal: Boolean,
          mention: String,
          moyenne: !Number,
          note: [
            {
              codeMod: String,
              note: String
            }
          ]
        },
        S2: {
          isVal: Boolean,
          mention: String,
          moyenne: !Number,
          note: [
            {
              codeMod: String,
              note: String
            }
          ]
        }
      },
      L2: {
        isVal: Boolean,
        mention: String,
        moyenne: Number,
        S3: {
          isVal: Boolean,
          mention: String,
          moyenne: !Number,
          note: [
            {
              codeMod: String,
              note: Number
            }
          ]
        },
        S4: {
          isVal: Boolean,
          mention: String,
          moyenne: !Number,
          note: [
            {
              codeMod: String,
              note: Number
            }
          ]
        }
      },
      L3: {
        isVal: Boolean,
        mention: String,
        moyenne: Number,
        S5: {
          isVal: Boolean,
          mention: String,
          moyenne: !Number,
          note: [
            {
              codeMod: String,
              note: Number
            }
          ]
        },
        S6: {
          isVal: Boolean,
          mention: String,
          moyenne: !Number,
          note: [
            {
              codeMod: String,
              note: Number
            }
          ]
        }
      }
    }
  }
})
let UniversiteSchema = new SimpleSchema({
  nom: !String,
  anneeUniv: !String,
  semestre: !Number,
  session: !String,
  filiere: !Object,
  modules: !Object
})
let EmployerSchema = new SimpleSchema({
  codeEmp: !String,
  type: !String,
  userName: !String,
  password: !String,
  nom: !String,
  prenom: !String,
  role: ![Object]
})


