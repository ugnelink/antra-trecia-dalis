# antra-trecia-dalis

#pragma once
#ifndef DUOMENYS_H_INCLUDED
#define DUOMENYS_H_INCLUDED

#include "funkcijos.h"

struct duomenys
{
    string Vardai;
    string Pavardes;
    vector<string> Pazymiai;
};

#endif

#include "funkcijos.h"

double vid(int egzaminas, vector<int>nd)
{
    double v;
    v = accumulate(nd.begin(), nd.end(), 0.000) / nd.size();

    return v;
}

double gal_rez(int egzaminas, vector<int> nd)
{
    double vidurkis, galutinis1;

    vidurkis = accumulate(nd.begin(), nd.end(), 0.000) / nd.size();
    galutinis1 = (0.4 * vidurkis) + (0.6 * egzaminas);

    return galutinis1;
}

double gal_mediana(int egzaminas, vector<int> nd)
{
    vector<double> skaiciai;
    for (int i = 0; i < nd.size(); i++) {
        skaiciai.push_back(nd.at(i));
    }

    skaiciai.push_back(egzaminas);

    sort(skaiciai.begin(), skaiciai.end());

    if (skaiciai.size() % 2 == 0)
    {
        return (skaiciai[skaiciai.size() / 2 - 1] + skaiciai[skaiciai.size() / 2]) / 2;
    }
    else
    {
        return skaiciai[skaiciai.size() / 2];
    }
}
void spausdinimas(vector<string> Vardai, vector<string> Pavardes, vector<double>galutinis1, vector<double> galutiniai, vector<double> galutiniai2)
{
    cout << setw(10) << "Vardas" << setw(25) << "Pavarde" << setw(25) << "Galutinis" << setw(25) << "Vidurkis" << setw(25) << "Mediana" << endl;
    cout << "---------------------------------------------------------------------------------------------------------\n";
    for (int i = 0; i < vardai.size(); i++) {

        cout << setw(5) << vardai[i] << setw(25) << pavardes[i] << setw(25) << galutinis1[i] << setw(25) << galutiniai[i] << setw(25) << galutiniai2[i] << endl;

    }
    
    
#pragma once
#ifndef FUNKCIJOS_H_INCLUDED
#define FUNKCIJOS_H_INCLUDED


using namespace std;

#include <string>
#include <iostream>
#include <vector>
#include <numeric>
#include <iomanip>
#include <cstdlib>
#include <iostream>
#include <cstdio>
#include <sstream>
    
    
#pragma once
#ifndef RUSIAVIMAS_H_INCLUDED
#define RUSIAVIMAS_H_INCLUDED

#include "funkcijos.h"

struct rusiavimas
{
    string Vardai;
    string Pavardes;
    double Vidurkiai;
    double Medianos;
};

#endif

#pragma once
#ifndef STUDENTAS_H_INCLUDED
#define STUDENTAS_H_INCLUDED

#include "funkcijos.h"

struct studentas
{
    string Vardai;
    string Pavardes;
    vector<int> Pazymiai;
};

#endif




