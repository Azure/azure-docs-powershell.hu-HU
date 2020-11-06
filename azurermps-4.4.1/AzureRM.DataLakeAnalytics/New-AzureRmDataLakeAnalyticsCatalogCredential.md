---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 1668ca10c8c3425bea7c4082033abb19f8de7306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493535"
---
# <span data-ttu-id="2f1e0-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="2f1e0-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="2f1e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="2f1e0-103">Létrehoz egy új Azure Data Lake Analytics katalógust.</span><span class="sxs-lookup"><span data-stu-id="2f1e0-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f1e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f1e0-104">SYNTAX</span></span>

### <span data-ttu-id="2f1e0-105">Az állomás nevének és portjának megadása (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f1e0-105">Specify host name and port (Default)</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f1e0-106">Teljes URI megadása</span><span class="sxs-lookup"><span data-stu-id="2f1e0-106">Specify full URI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f1e0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f1e0-107">DESCRIPTION</span></span>
<span data-ttu-id="2f1e0-108">A New-AzureRmDataLakeAnalyticsCatalogCredential parancsmag új hitelesítő adatokat hoz létre az Azure Data Lake-tó elemzési katalógusában a külső adatforrásokhoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="2f1e0-108">The New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="2f1e0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2f1e0-109">EXAMPLES</span></span>

### <span data-ttu-id="2f1e0-110">Példa 1: az állomást és a portot megadó katalógus hitelesítő adatainak létrehozása</span><span class="sxs-lookup"><span data-stu-id="2f1e0-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="2f1e0-111">Ezzel a paranccsal létrehozhatja az adott fiók, adatbázis, állomás és port megadott hitelesítő adatait HTTPS protokoll használatával.</span><span class="sxs-lookup"><span data-stu-id="2f1e0-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="2f1e0-112">2. példa: hitelesítő adatok létrehozása a teljes URI-t megadó katalógushoz</span><span class="sxs-lookup"><span data-stu-id="2f1e0-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="2f1e0-113">Ezzel a paranccsal létrehozhatja a megadott fiók, adatbázis és külső adatforrás URI-azonosítójának megadott hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="2f1e0-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="2f1e0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f1e0-114">PARAMETERS</span></span>

### <span data-ttu-id="2f1e0-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="2f1e0-115">-Account</span></span>
<span data-ttu-id="2f1e0-116">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f1e0-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="2f1e0-117">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="2f1e0-117">-Credential</span></span>
<span data-ttu-id="2f1e0-118">A hitelesítő adatok felhasználónevét és a hozzá tartozó jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f1e0-118">Specifies the user name and corresponding password of the credential.</span></span>

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

### <span data-ttu-id="2f1e0-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="2f1e0-119">-CredentialName</span></span>
<span data-ttu-id="2f1e0-120">A hitelesítő adatok nevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f1e0-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="2f1e0-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="2f1e0-121">-DatabaseHost</span></span>
<span data-ttu-id="2f1e0-122">Annak a külső adatforrásnak az állomásnevét adja meg, amely a hitelesítő adatokhoz kapcsolódhat a mydatabase.contoso.com formázása mezőben.</span><span class="sxs-lookup"><span data-stu-id="2f1e0-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f1e0-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f1e0-123">-DatabaseName</span></span>
<span data-ttu-id="2f1e0-124">Adja meg az adatbázis nevét az adattó-statisztika félrecsapott, hogy a hitelesítő adatok tárolása megtörténik.</span><span class="sxs-lookup"><span data-stu-id="2f1e0-124">Specifies the name of the database in the Data Lake Analytics acocunt that the credential will be stored in.</span></span>

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

### <span data-ttu-id="2f1e0-125">-Port</span><span class="sxs-lookup"><span data-stu-id="2f1e0-125">-Port</span></span>
<span data-ttu-id="2f1e0-126">Annak a portnak a portszámát adja meg, amely az adott DatabaseHost a hitelesítő adatokkal való csatlakozáshoz használható.</span><span class="sxs-lookup"><span data-stu-id="2f1e0-126">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f1e0-127">-URI</span><span class="sxs-lookup"><span data-stu-id="2f1e0-127">-Uri</span></span>
<span data-ttu-id="2f1e0-128">Annak a külső adatforrásnak a teljes egységes erőforrás-azonosítóját adja meg, amelyhez a hitelesítő adatok csatlakozni tudnak.</span><span class="sxs-lookup"><span data-stu-id="2f1e0-128">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f1e0-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f1e0-129">-Confirm</span></span>
<span data-ttu-id="2f1e0-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f1e0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f1e0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f1e0-131">-WhatIf</span></span>
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

### <span data-ttu-id="2f1e0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f1e0-132">-DefaultProfile</span></span>
<span data-ttu-id="2f1e0-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f1e0-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f1e0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f1e0-134">CommonParameters</span></span>
<span data-ttu-id="2f1e0-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f1e0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f1e0-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f1e0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f1e0-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f1e0-137">INPUTS</span></span>

## <span data-ttu-id="2f1e0-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f1e0-138">OUTPUTS</span></span>

### <span data-ttu-id="2f1e0-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="2f1e0-139">None</span></span>

## <span data-ttu-id="2f1e0-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f1e0-140">NOTES</span></span>

## <span data-ttu-id="2f1e0-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f1e0-141">RELATED LINKS</span></span>

