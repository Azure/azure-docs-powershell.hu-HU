---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 9547a3f3aed86bd7458f9fbf1f1a4375e2d95086
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012083"
---
# <span data-ttu-id="14f6a-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="14f6a-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="14f6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="14f6a-103">Beállítja egy eszköz tárolási fiókjának hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="14f6a-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="14f6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14f6a-104">SYNTAX</span></span>

### <span data-ttu-id="14f6a-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="14f6a-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14f6a-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14f6a-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14f6a-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14f6a-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14f6a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="14f6a-108">DESCRIPTION</span></span>
<span data-ttu-id="14f6a-109">A **set-AzDataBoxEdgeStorageAccountCredential** parancsmag a tárolási fiók hitelesítő adatait az adatok mező szélén lévő eszközön frissíti.</span><span class="sxs-lookup"><span data-stu-id="14f6a-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="14f6a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="14f6a-110">EXAMPLES</span></span>

### <span data-ttu-id="14f6a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="14f6a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="14f6a-112">Segítséget nyújt a tárolási fiókok elérési kulcsainak elforgatásához</span><span class="sxs-lookup"><span data-stu-id="14f6a-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="14f6a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14f6a-113">PARAMETERS</span></span>

### <span data-ttu-id="14f6a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14f6a-114">-AsJob</span></span>
<span data-ttu-id="14f6a-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="14f6a-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f6a-116">-DefaultProfile</span></span>
<span data-ttu-id="14f6a-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14f6a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14f6a-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="14f6a-118">-DeviceName</span></span>
<span data-ttu-id="14f6a-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="14f6a-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14f6a-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="14f6a-120">-EncryptionKey</span></span>
<span data-ttu-id="14f6a-121">Az Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="14f6a-121">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f6a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14f6a-122">-InputObject</span></span>
<span data-ttu-id="14f6a-123">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="14f6a-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14f6a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="14f6a-124">-Name</span></span>
<span data-ttu-id="14f6a-125">A használandó tárterület-fiók neve</span><span class="sxs-lookup"><span data-stu-id="14f6a-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14f6a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14f6a-126">-ResourceGroupName</span></span>
<span data-ttu-id="14f6a-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="14f6a-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14f6a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14f6a-128">-ResourceId</span></span>
<span data-ttu-id="14f6a-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="14f6a-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14f6a-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="14f6a-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="14f6a-131">tárolási fiók elérési kulcsának biztosítása</span><span class="sxs-lookup"><span data-stu-id="14f6a-131">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f6a-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="14f6a-132">-Confirm</span></span>
<span data-ttu-id="14f6a-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="14f6a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14f6a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14f6a-134">-WhatIf</span></span>
<span data-ttu-id="14f6a-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="14f6a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14f6a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14f6a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14f6a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f6a-137">CommonParameters</span></span>
<span data-ttu-id="14f6a-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14f6a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f6a-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="14f6a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f6a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14f6a-140">INPUTS</span></span>

### <span data-ttu-id="14f6a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="14f6a-141">System.String</span></span>

### <span data-ttu-id="14f6a-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="14f6a-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="14f6a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14f6a-143">OUTPUTS</span></span>

### <span data-ttu-id="14f6a-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="14f6a-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="14f6a-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14f6a-145">NOTES</span></span>

## <span data-ttu-id="14f6a-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14f6a-146">RELATED LINKS</span></span>
