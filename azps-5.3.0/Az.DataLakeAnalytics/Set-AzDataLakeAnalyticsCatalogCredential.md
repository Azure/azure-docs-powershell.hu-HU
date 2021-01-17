---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 8d188e2f19c04792ea29cadef9d9ef71c20cfce9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480298"
---
# <span data-ttu-id="5f6f3-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="5f6f3-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="5f6f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6f3-103">Módosítja az Azure Data Lake Analytics-katalógus hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="5f6f3-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="5f6f3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5f6f3-104">SYNTAX</span></span>

### <span data-ttu-id="5f6f3-105">SetByHostNameAndPort (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5f6f3-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f6f3-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="5f6f3-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f6f3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5f6f3-107">DESCRIPTION</span></span>
<span data-ttu-id="5f6f3-108">A Set-AzDataLakeAnalyticsCatalogCredential parancsmag módosítja az Azure Data Lake Analytics-katalógushoz társított hitelesítőadat-jelszót.</span><span class="sxs-lookup"><span data-stu-id="5f6f3-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="5f6f3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5f6f3-109">EXAMPLES</span></span>

### <span data-ttu-id="5f6f3-110">1. példa: Fiókhoz társított hitelesítő adatok jelszavának módosítása</span><span class="sxs-lookup"><span data-stu-id="5f6f3-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="5f6f3-111">Ez a parancs a Hitelesítőadat-jelszót a NewPasswordban megadott jelszóra állítja.</span><span class="sxs-lookup"><span data-stu-id="5f6f3-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="5f6f3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f6f3-112">PARAMETERS</span></span>

### <span data-ttu-id="5f6f3-113">-Account</span><span class="sxs-lookup"><span data-stu-id="5f6f3-113">-Account</span></span>
<span data-ttu-id="5f6f3-114">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f6f3-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="5f6f3-115">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="5f6f3-115">-Credential</span></span>
<span data-ttu-id="5f6f3-116">A módosítani szükséges hitelesítő adatok nevét és aktuális jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f6f3-116">Specifies the name and current password of the credential to modify.</span></span>

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

### <span data-ttu-id="5f6f3-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="5f6f3-117">-CredentialName</span></span>
<span data-ttu-id="5f6f3-118">A módosítani szükséges hitelesítő adat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f6f3-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="5f6f3-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="5f6f3-119">-DatabaseHost</span></span>
<span data-ttu-id="5f6f3-120">Megadja annak a külső adatforrásnak az állomásnevét, amelyhez a hitelesítő adatok a következő formátumban mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="5f6f3-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f3-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5f6f3-121">-DatabaseName</span></span>
<span data-ttu-id="5f6f3-122">Megadja a hitelesítő adatokat tároló Data Lake Analytics-fiókban található adatbázis nevét.</span><span class="sxs-lookup"><span data-stu-id="5f6f3-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="5f6f3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f6f3-123">-DefaultProfile</span></span>
<span data-ttu-id="5f6f3-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5f6f3-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f6f3-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="5f6f3-125">-NewPassword</span></span>
<span data-ttu-id="5f6f3-126">A hitelesítő adatok új jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f6f3-126">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="5f6f3-127">-Port</span><span class="sxs-lookup"><span data-stu-id="5f6f3-127">-Port</span></span>
<span data-ttu-id="5f6f3-128">A megadott DatabaseHost-kiszolgálóhoz való csatlakozáshoz használt portszám megadása ezen hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="5f6f3-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f3-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="5f6f3-129">-Uri</span></span>
<span data-ttu-id="5f6f3-130">Megadja annak a külső adatforrásnak a teljes egységes erőforrás-azonosítóját (URI), amelyhez ez a hitelesítő adat kapcsolódhat.</span><span class="sxs-lookup"><span data-stu-id="5f6f3-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: SetByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f6f3-131">-Confirm</span></span>
<span data-ttu-id="5f6f3-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5f6f3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f6f3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f6f3-133">-WhatIf</span></span>
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

### <span data-ttu-id="5f6f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6f3-134">CommonParameters</span></span>
<span data-ttu-id="5f6f3-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f6f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6f3-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f6f3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6f3-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f6f3-137">INPUTS</span></span>

### <span data-ttu-id="5f6f3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5f6f3-138">System.String</span></span>

### <span data-ttu-id="5f6f3-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="5f6f3-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="5f6f3-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="5f6f3-140">System.Uri</span></span>

### <span data-ttu-id="5f6f3-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="5f6f3-141">System.Int32</span></span>

## <span data-ttu-id="5f6f3-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f6f3-142">OUTPUTS</span></span>

### <span data-ttu-id="5f6f3-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="5f6f3-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="5f6f3-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5f6f3-144">NOTES</span></span>

## <span data-ttu-id="5f6f3-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f6f3-145">RELATED LINKS</span></span>
