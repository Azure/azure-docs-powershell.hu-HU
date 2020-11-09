---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 8d188e2f19c04792ea29cadef9d9ef71c20cfce9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298007"
---
# <span data-ttu-id="b7b58-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="b7b58-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="b7b58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7b58-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b58-103">Az Azure Data Lake Analytics katalógusa hitelesítő adatait tartalmazó jelszó módosítása.</span><span class="sxs-lookup"><span data-stu-id="b7b58-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="b7b58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7b58-104">SYNTAX</span></span>

### <span data-ttu-id="b7b58-105">SetByHostNameAndPort (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7b58-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7b58-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="b7b58-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7b58-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7b58-107">DESCRIPTION</span></span>
<span data-ttu-id="b7b58-108">A Set-AzDataLakeAnalyticsCatalogCredential parancsmag módosítja az Azure Data Lake Analytics katalógushoz társított hitelesítő jelszót.</span><span class="sxs-lookup"><span data-stu-id="b7b58-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="b7b58-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b7b58-109">EXAMPLES</span></span>

### <span data-ttu-id="b7b58-110">1. példa: a hitelesítő adatokhoz társított jelszó módosítása a fiókhoz</span><span class="sxs-lookup"><span data-stu-id="b7b58-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="b7b58-111">Ez a parancs beállítja a hitelesítő jelszót a NewPassword megadott jelszóhoz.</span><span class="sxs-lookup"><span data-stu-id="b7b58-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="b7b58-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7b58-112">PARAMETERS</span></span>

### <span data-ttu-id="b7b58-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="b7b58-113">-Account</span></span>
<span data-ttu-id="b7b58-114">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7b58-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="b7b58-115">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="b7b58-115">-Credential</span></span>
<span data-ttu-id="b7b58-116">A módosítani kívánt hitelesítő adatok nevét és aktuális jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7b58-116">Specifies the name and current password of the credential to modify.</span></span>

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

### <span data-ttu-id="b7b58-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="b7b58-117">-CredentialName</span></span>
<span data-ttu-id="b7b58-118">A módosítani kívánt hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7b58-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="b7b58-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="b7b58-119">-DatabaseHost</span></span>
<span data-ttu-id="b7b58-120">Annak a külső adatforrásnak az állomásnevét adja meg, amely a hitelesítő adatokhoz kapcsolódhat a mydatabase.contoso.com formázása mezőben.</span><span class="sxs-lookup"><span data-stu-id="b7b58-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="b7b58-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7b58-121">-DatabaseName</span></span>
<span data-ttu-id="b7b58-122">Annak az adatbázisnak a nevét adja meg, amely a hitelesítő adatokat tároló adattói Analytics-fiókban van.</span><span class="sxs-lookup"><span data-stu-id="b7b58-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="b7b58-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b58-123">-DefaultProfile</span></span>
<span data-ttu-id="b7b58-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b7b58-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7b58-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="b7b58-125">-NewPassword</span></span>
<span data-ttu-id="b7b58-126">A hitelesítő adatok új jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7b58-126">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="b7b58-127">-Port</span><span class="sxs-lookup"><span data-stu-id="b7b58-127">-Port</span></span>
<span data-ttu-id="b7b58-128">Annak a portnak a portszámát adja meg, amely az adott DatabaseHost a hitelesítő adatokkal való csatlakozáshoz használható.</span><span class="sxs-lookup"><span data-stu-id="b7b58-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="b7b58-129">-URI</span><span class="sxs-lookup"><span data-stu-id="b7b58-129">-Uri</span></span>
<span data-ttu-id="b7b58-130">Annak a külső adatforrásnak a teljes egységes erőforrás-azonosítóját adja meg, amelyhez a hitelesítő adatok csatlakozni tudnak.</span><span class="sxs-lookup"><span data-stu-id="b7b58-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="b7b58-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7b58-131">-Confirm</span></span>
<span data-ttu-id="b7b58-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7b58-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7b58-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7b58-133">-WhatIf</span></span>
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

### <span data-ttu-id="b7b58-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b58-134">CommonParameters</span></span>
<span data-ttu-id="b7b58-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7b58-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b58-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7b58-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b58-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7b58-137">INPUTS</span></span>

### <span data-ttu-id="b7b58-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b7b58-138">System.String</span></span>

### <span data-ttu-id="b7b58-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="b7b58-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="b7b58-140">System. URI</span><span class="sxs-lookup"><span data-stu-id="b7b58-140">System.Uri</span></span>

### <span data-ttu-id="b7b58-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b7b58-141">System.Int32</span></span>

## <span data-ttu-id="b7b58-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7b58-142">OUTPUTS</span></span>

### <span data-ttu-id="b7b58-143">Microsoft. Azure. Management. DataLake. Analytics. models. USqlCredential</span><span class="sxs-lookup"><span data-stu-id="b7b58-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="b7b58-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7b58-144">NOTES</span></span>

## <span data-ttu-id="b7b58-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7b58-145">RELATED LINKS</span></span>
