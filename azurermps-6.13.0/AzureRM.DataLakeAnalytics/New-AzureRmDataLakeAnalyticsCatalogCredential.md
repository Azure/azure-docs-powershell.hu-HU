---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 2d239e8c40c4e2472ee26a2f08b14a8f7871bd80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502127"
---
# <span data-ttu-id="4a91e-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="4a91e-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="4a91e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a91e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a91e-103">Létrehoz egy új Azure Data Lake Analytics katalógust.</span><span class="sxs-lookup"><span data-stu-id="4a91e-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a91e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a91e-104">SYNTAX</span></span>

### <span data-ttu-id="4a91e-105">CreateByHostNameAndPort (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4a91e-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a91e-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="4a91e-106">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a91e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a91e-107">DESCRIPTION</span></span>
<span data-ttu-id="4a91e-108">A New-AzureRmDataLakeAnalyticsCatalogCredential parancsmag új hitelesítő adatokat hoz létre az Azure Data Lake-tó elemzési katalógusában a külső adatforrásokhoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="4a91e-108">The New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="4a91e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4a91e-109">EXAMPLES</span></span>

### <span data-ttu-id="4a91e-110">Példa 1: az állomást és a portot megadó katalógus hitelesítő adatainak létrehozása</span><span class="sxs-lookup"><span data-stu-id="4a91e-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="4a91e-111">Ezzel a paranccsal létrehozhatja az adott fiók, adatbázis, állomás és port megadott hitelesítő adatait HTTPS protokoll használatával.</span><span class="sxs-lookup"><span data-stu-id="4a91e-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="4a91e-112">2. példa: hitelesítő adatok létrehozása a teljes URI-t megadó katalógushoz</span><span class="sxs-lookup"><span data-stu-id="4a91e-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="4a91e-113">Ezzel a paranccsal létrehozhatja a megadott fiók, adatbázis és külső adatforrás URI-azonosítójának megadott hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="4a91e-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="4a91e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a91e-114">PARAMETERS</span></span>

### <span data-ttu-id="4a91e-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="4a91e-115">-Account</span></span>
<span data-ttu-id="4a91e-116">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a91e-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4a91e-117">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="4a91e-117">-Credential</span></span>
<span data-ttu-id="4a91e-118">A hitelesítő adatok felhasználónevét és a hozzá tartozó jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a91e-118">Specifies the user name and corresponding password of the credential.</span></span>

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

### <span data-ttu-id="4a91e-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="4a91e-119">-CredentialName</span></span>
<span data-ttu-id="4a91e-120">A hitelesítő adatok nevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a91e-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="4a91e-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="4a91e-121">-DatabaseHost</span></span>
<span data-ttu-id="4a91e-122">Annak a külső adatforrásnak az állomásnevét adja meg, amely a hitelesítő adatokhoz kapcsolódhat a mydatabase.contoso.com formázása mezőben.</span><span class="sxs-lookup"><span data-stu-id="4a91e-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="4a91e-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a91e-123">-DatabaseName</span></span>
<span data-ttu-id="4a91e-124">Annak az adatbázisnak a nevét adja meg, amely a hitelesítő adatokat tároló adattói Analytics-fiókban található.</span><span class="sxs-lookup"><span data-stu-id="4a91e-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

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

### <span data-ttu-id="4a91e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a91e-125">-DefaultProfile</span></span>
<span data-ttu-id="4a91e-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4a91e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a91e-127">-Port</span><span class="sxs-lookup"><span data-stu-id="4a91e-127">-Port</span></span>
<span data-ttu-id="4a91e-128">Annak a portnak a portszámát adja meg, amely az adott DatabaseHost a hitelesítő adatokkal való csatlakozáshoz használható.</span><span class="sxs-lookup"><span data-stu-id="4a91e-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="4a91e-129">-URI</span><span class="sxs-lookup"><span data-stu-id="4a91e-129">-Uri</span></span>
<span data-ttu-id="4a91e-130">Annak a külső adatforrásnak a teljes egységes erőforrás-azonosítóját adja meg, amelyhez a hitelesítő adatok csatlakozni tudnak.</span><span class="sxs-lookup"><span data-stu-id="4a91e-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="4a91e-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4a91e-131">-Confirm</span></span>
<span data-ttu-id="4a91e-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4a91e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a91e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a91e-133">-WhatIf</span></span>
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

### <span data-ttu-id="4a91e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a91e-134">CommonParameters</span></span>
<span data-ttu-id="4a91e-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a91e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a91e-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a91e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a91e-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a91e-137">INPUTS</span></span>

### <span data-ttu-id="4a91e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4a91e-138">System.String</span></span>

### <span data-ttu-id="4a91e-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="4a91e-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="4a91e-140">System. URI</span><span class="sxs-lookup"><span data-stu-id="4a91e-140">System.Uri</span></span>

### <span data-ttu-id="4a91e-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4a91e-141">System.Int32</span></span>

## <span data-ttu-id="4a91e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a91e-142">OUTPUTS</span></span>

### <span data-ttu-id="4a91e-143">Microsoft. Azure. Management. DataLake. Analytics. models. USqlCredential</span><span class="sxs-lookup"><span data-stu-id="4a91e-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="4a91e-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a91e-144">NOTES</span></span>

## <span data-ttu-id="4a91e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a91e-145">RELATED LINKS</span></span>
