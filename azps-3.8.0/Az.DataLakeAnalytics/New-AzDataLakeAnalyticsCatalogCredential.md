---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 4f7a391228529cdb28951b6b3f3f792e8d0de395
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010841"
---
# <span data-ttu-id="5e1d5-101">New-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="5e1d5-101">New-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="5e1d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e1d5-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1d5-103">Létrehoz egy új Azure Data Lake Analytics katalógust.</span><span class="sxs-lookup"><span data-stu-id="5e1d5-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="5e1d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e1d5-104">SYNTAX</span></span>

### <span data-ttu-id="5e1d5-105">CreateByHostNameAndPort (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5e1d5-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e1d5-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="5e1d5-106">CreateByFullURI</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e1d5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e1d5-107">DESCRIPTION</span></span>
<span data-ttu-id="5e1d5-108">A New-AzDataLakeAnalyticsCatalogCredential parancsmag új hitelesítő adatokat hoz létre az Azure Data Lake-tó elemzési katalógusában a külső adatforrásokhoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="5e1d5-108">The New-AzDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="5e1d5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5e1d5-109">EXAMPLES</span></span>

### <span data-ttu-id="5e1d5-110">Példa 1: az állomást és a portot megadó katalógus hitelesítő adatainak létrehozása</span><span class="sxs-lookup"><span data-stu-id="5e1d5-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="5e1d5-111">Ezzel a paranccsal létrehozhatja az adott fiók, adatbázis, állomás és port megadott hitelesítő adatait HTTPS protokoll használatával.</span><span class="sxs-lookup"><span data-stu-id="5e1d5-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="5e1d5-112">2. példa: hitelesítő adatok létrehozása a teljes URI-t megadó katalógushoz</span><span class="sxs-lookup"><span data-stu-id="5e1d5-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="5e1d5-113">Ezzel a paranccsal létrehozhatja a megadott fiók, adatbázis és külső adatforrás URI-azonosítójának megadott hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="5e1d5-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="5e1d5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e1d5-114">PARAMETERS</span></span>

### <span data-ttu-id="5e1d5-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="5e1d5-115">-Account</span></span>
<span data-ttu-id="5e1d5-116">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e1d5-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="5e1d5-117">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="5e1d5-117">-Credential</span></span>
<span data-ttu-id="5e1d5-118">A hitelesítő adatok felhasználónevét és a hozzá tartozó jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e1d5-118">Specifies the user name and corresponding password of the credential.</span></span>

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

### <span data-ttu-id="5e1d5-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="5e1d5-119">-CredentialName</span></span>
<span data-ttu-id="5e1d5-120">A hitelesítő adatok nevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e1d5-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="5e1d5-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="5e1d5-121">-DatabaseHost</span></span>
<span data-ttu-id="5e1d5-122">Annak a külső adatforrásnak az állomásnevét adja meg, amely a hitelesítő adatokhoz kapcsolódhat a mydatabase.contoso.com formázása mezőben.</span><span class="sxs-lookup"><span data-stu-id="5e1d5-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="5e1d5-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5e1d5-123">-DatabaseName</span></span>
<span data-ttu-id="5e1d5-124">Annak az adatbázisnak a nevét adja meg, amely a hitelesítő adatokat tároló adattói Analytics-fiókban található.</span><span class="sxs-lookup"><span data-stu-id="5e1d5-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

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

### <span data-ttu-id="5e1d5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e1d5-125">-DefaultProfile</span></span>
<span data-ttu-id="5e1d5-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5e1d5-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e1d5-127">-Port</span><span class="sxs-lookup"><span data-stu-id="5e1d5-127">-Port</span></span>
<span data-ttu-id="5e1d5-128">Annak a portnak a portszámát adja meg, amely az adott DatabaseHost a hitelesítő adatokkal való csatlakozáshoz használható.</span><span class="sxs-lookup"><span data-stu-id="5e1d5-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="5e1d5-129">-URI</span><span class="sxs-lookup"><span data-stu-id="5e1d5-129">-Uri</span></span>
<span data-ttu-id="5e1d5-130">Annak a külső adatforrásnak a teljes egységes erőforrás-azonosítóját adja meg, amelyhez a hitelesítő adatok csatlakozni tudnak.</span><span class="sxs-lookup"><span data-stu-id="5e1d5-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="5e1d5-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5e1d5-131">-Confirm</span></span>
<span data-ttu-id="5e1d5-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5e1d5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e1d5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e1d5-133">-WhatIf</span></span>
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

### <span data-ttu-id="5e1d5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1d5-134">CommonParameters</span></span>
<span data-ttu-id="5e1d5-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e1d5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1d5-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e1d5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1d5-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e1d5-137">INPUTS</span></span>

### <span data-ttu-id="5e1d5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5e1d5-138">System.String</span></span>

### <span data-ttu-id="5e1d5-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="5e1d5-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="5e1d5-140">System. URI</span><span class="sxs-lookup"><span data-stu-id="5e1d5-140">System.Uri</span></span>

### <span data-ttu-id="5e1d5-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5e1d5-141">System.Int32</span></span>

## <span data-ttu-id="5e1d5-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e1d5-142">OUTPUTS</span></span>

### <span data-ttu-id="5e1d5-143">Microsoft. Azure. Management. DataLake. Analytics. models. USqlCredential</span><span class="sxs-lookup"><span data-stu-id="5e1d5-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="5e1d5-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e1d5-144">NOTES</span></span>

## <span data-ttu-id="5e1d5-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e1d5-145">RELATED LINKS</span></span>
