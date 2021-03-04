---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: d5fe98e6c8514ced094700e4633ebbd2e7f1d197
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930089"
---
# <span data-ttu-id="b41ed-101">New-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="b41ed-101">New-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="b41ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b41ed-102">SYNOPSIS</span></span>
<span data-ttu-id="b41ed-103">Létrehozza az Azure Data Lake Analytics katalógusának új hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="b41ed-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="b41ed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b41ed-104">SYNTAX</span></span>

### <span data-ttu-id="b41ed-105">CreateByHostNameAndPort (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b41ed-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b41ed-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="b41ed-106">CreateByFullURI</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b41ed-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b41ed-107">DESCRIPTION</span></span>
<span data-ttu-id="b41ed-108">A New-AzDataLakeAnalyticsCatalogCredential parancsmag létrehoz egy új hitelesítő adatokat egy Azure Data Lake Analytics katalógusban külső adatforráshoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="b41ed-108">The New-AzDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="b41ed-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b41ed-109">EXAMPLES</span></span>

### <span data-ttu-id="b41ed-110">1. példa: Hitelesítő adatok létrehozása az állomást és portot meg tároló katalógushoz</span><span class="sxs-lookup"><span data-stu-id="b41ed-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="b41ed-111">Ez a parancs létrehozza a megadott fiókhoz, adatbázishoz, állomáshoz és porthoz a https protokollt használó hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b41ed-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="b41ed-112">2. példa: Hitelesítő adatok létrehozása a teljes URI azonosítót meg tároló katalógushoz</span><span class="sxs-lookup"><span data-stu-id="b41ed-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="b41ed-113">Ez a parancs létrehozza a megadott fiókhoz, adatbázishoz és külső adatforrás URI-hoz megadott hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b41ed-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="b41ed-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b41ed-114">PARAMETERS</span></span>

### <span data-ttu-id="b41ed-115">-Account</span><span class="sxs-lookup"><span data-stu-id="b41ed-115">-Account</span></span>
<span data-ttu-id="b41ed-116">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b41ed-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41ed-117">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="b41ed-117">-Credential</span></span>
<span data-ttu-id="b41ed-118">A hitelesítő adatok felhasználónevét és megfelelő jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b41ed-118">Specifies the user name and corresponding password of the credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41ed-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="b41ed-119">-CredentialName</span></span>
<span data-ttu-id="b41ed-120">A hitelesítő adatok nevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b41ed-120">Specifies the name and password of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41ed-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="b41ed-121">-DatabaseHost</span></span>
<span data-ttu-id="b41ed-122">Megadja annak a külső adatforrásnak az állomásnevét, amelyhez a hitelesítő adatok a következő formátumban mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="b41ed-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41ed-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b41ed-123">-DatabaseName</span></span>
<span data-ttu-id="b41ed-124">Annak az adatbázisnak a nevét adja meg a Data Lake Analytics-fiókban, amely a hitelesítő adatokat tárolja.</span><span class="sxs-lookup"><span data-stu-id="b41ed-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41ed-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b41ed-125">-DefaultProfile</span></span>
<span data-ttu-id="b41ed-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b41ed-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41ed-127">-Port</span><span class="sxs-lookup"><span data-stu-id="b41ed-127">-Port</span></span>
<span data-ttu-id="b41ed-128">A megadott DatabaseHost-kiszolgálóhoz való csatlakozáshoz használt portszám megadása ezen hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="b41ed-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41ed-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="b41ed-129">-Uri</span></span>
<span data-ttu-id="b41ed-130">Megadja annak a külső adatforrásnak a teljes egységes erőforrás-azonosítóját (URI), amelyhez ez a hitelesítő adat kapcsolódhat.</span><span class="sxs-lookup"><span data-stu-id="b41ed-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41ed-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b41ed-131">-Confirm</span></span>
<span data-ttu-id="b41ed-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b41ed-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41ed-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b41ed-133">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41ed-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b41ed-134">CommonParameters</span></span>
<span data-ttu-id="b41ed-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b41ed-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b41ed-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b41ed-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b41ed-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b41ed-137">INPUTS</span></span>

### <span data-ttu-id="b41ed-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b41ed-138">System.String</span></span>

### <span data-ttu-id="b41ed-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="b41ed-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="b41ed-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="b41ed-140">System.Uri</span></span>

### <span data-ttu-id="b41ed-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b41ed-141">System.Int32</span></span>

## <span data-ttu-id="b41ed-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b41ed-142">OUTPUTS</span></span>

### <span data-ttu-id="b41ed-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="b41ed-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="b41ed-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b41ed-144">NOTES</span></span>

## <span data-ttu-id="b41ed-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b41ed-145">RELATED LINKS</span></span>
