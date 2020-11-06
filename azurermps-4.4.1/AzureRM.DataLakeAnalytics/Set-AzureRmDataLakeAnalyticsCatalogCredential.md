---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: e82559ec366809613ba66af4c27a3b944869f074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501911"
---
# <span data-ttu-id="cc689-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="cc689-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="cc689-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc689-102">SYNOPSIS</span></span>
<span data-ttu-id="cc689-103">Az Azure Data Lake Analytics katalógusa hitelesítő adatait tartalmazó jelszó módosítása.</span><span class="sxs-lookup"><span data-stu-id="cc689-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc689-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc689-104">SYNTAX</span></span>

### <span data-ttu-id="cc689-105">Az állomás nevének és portjának megadása (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc689-105">Specify host name and port (Default)</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc689-106">Teljes URI megadása</span><span class="sxs-lookup"><span data-stu-id="cc689-106">Specify full URI</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc689-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc689-107">DESCRIPTION</span></span>
<span data-ttu-id="cc689-108">A Set-AzureRmDataLakeAnalyticsCatalogCredential parancsmag módosítja az Azure Data Lake Analytics katalógushoz társított hitelesítő jelszót.</span><span class="sxs-lookup"><span data-stu-id="cc689-108">The Set-AzureRmDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="cc689-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cc689-109">EXAMPLES</span></span>

### <span data-ttu-id="cc689-110">1. példa: a hitelesítő adatokhoz társított jelszó módosítása a fiókhoz</span><span class="sxs-lookup"><span data-stu-id="cc689-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="cc689-111">Ez a parancs beállítja a hitelesítő jelszót a NewPassword megadott jelszóhoz.</span><span class="sxs-lookup"><span data-stu-id="cc689-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="cc689-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc689-112">PARAMETERS</span></span>

### <span data-ttu-id="cc689-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="cc689-113">-Account</span></span>
<span data-ttu-id="cc689-114">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc689-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="cc689-115">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="cc689-115">-Credential</span></span>
<span data-ttu-id="cc689-116">A módosítani kívánt hitelesítő adatok nevét és aktuális jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc689-116">Specifies the name and current password of the credential to modify.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc689-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="cc689-117">-CredentialName</span></span>
<span data-ttu-id="cc689-118">A módosítani kívánt hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc689-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="cc689-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="cc689-119">-DatabaseHost</span></span>
<span data-ttu-id="cc689-120">Annak a külső adatforrásnak az állomásnevét adja meg, amely a hitelesítő adatokhoz kapcsolódhat a mydatabase.contoso.com formázása mezőben.</span><span class="sxs-lookup"><span data-stu-id="cc689-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="cc689-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cc689-121">-DatabaseName</span></span>
<span data-ttu-id="cc689-122">Annak az adatbázisnak a nevét adja meg, amely a hitelesítő adatokat tároló adattói Analytics-fiókban van.</span><span class="sxs-lookup"><span data-stu-id="cc689-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="cc689-123">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="cc689-123">-NewPassword</span></span>
<span data-ttu-id="cc689-124">A hitelesítő adatok új jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc689-124">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="cc689-125">-Port</span><span class="sxs-lookup"><span data-stu-id="cc689-125">-Port</span></span>
<span data-ttu-id="cc689-126">Annak a portnak a portszámát adja meg, amely az adott DatabaseHost a hitelesítő adatokkal való csatlakozáshoz használható.</span><span class="sxs-lookup"><span data-stu-id="cc689-126">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="cc689-127">-URI</span><span class="sxs-lookup"><span data-stu-id="cc689-127">-Uri</span></span>
<span data-ttu-id="cc689-128">Annak a külső adatforrásnak a teljes egységes erőforrás-azonosítóját adja meg, amelyhez a hitelesítő adatok csatlakozni tudnak.</span><span class="sxs-lookup"><span data-stu-id="cc689-128">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="cc689-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc689-129">-Confirm</span></span>
<span data-ttu-id="cc689-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc689-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc689-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc689-131">-WhatIf</span></span>
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

### <span data-ttu-id="cc689-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc689-132">-DefaultProfile</span></span>
<span data-ttu-id="cc689-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc689-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc689-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc689-134">CommonParameters</span></span>
<span data-ttu-id="cc689-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc689-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc689-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc689-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc689-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc689-137">INPUTS</span></span>

## <span data-ttu-id="cc689-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc689-138">OUTPUTS</span></span>

### <span data-ttu-id="cc689-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="cc689-139">None</span></span>

## <span data-ttu-id="cc689-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc689-140">NOTES</span></span>

## <span data-ttu-id="cc689-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc689-141">RELATED LINKS</span></span>

