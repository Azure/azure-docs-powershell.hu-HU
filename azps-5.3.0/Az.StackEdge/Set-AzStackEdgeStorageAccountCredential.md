---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 89e727b836f28ac1972bcf15e872e2860a8a6672
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465921"
---
# <span data-ttu-id="25a8d-101">Set-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="25a8d-101">Set-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="25a8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="25a8d-103">Beállítja egy eszköz tárfiókja hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="25a8d-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="25a8d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="25a8d-104">SYNTAX</span></span>

### <span data-ttu-id="25a8d-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25a8d-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25a8d-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25a8d-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25a8d-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25a8d-107">SetByParentObjectParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25a8d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="25a8d-108">DESCRIPTION</span></span>
<span data-ttu-id="25a8d-109">A **Set-AzStackEdgeStorageAccountCredential** parancsmag frissíti a Stack Edge eszköz egyik tárfiókjára vonatkozó hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="25a8d-109">The **Set-AzStackEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Stack Edge device.</span></span>

## <span data-ttu-id="25a8d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="25a8d-110">EXAMPLES</span></span>

### <span data-ttu-id="25a8d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="25a8d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="25a8d-112">Segítség a tárfiókok hozzáférési kulcsának elforgatásában</span><span class="sxs-lookup"><span data-stu-id="25a8d-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="25a8d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25a8d-113">PARAMETERS</span></span>

### <span data-ttu-id="25a8d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25a8d-114">-AsJob</span></span>
<span data-ttu-id="25a8d-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="25a8d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25a8d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a8d-116">-DefaultProfile</span></span>
<span data-ttu-id="25a8d-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25a8d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25a8d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="25a8d-118">-DeviceName</span></span>
<span data-ttu-id="25a8d-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="25a8d-119">Device Name</span></span>

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

### <span data-ttu-id="25a8d-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="25a8d-120">-EncryptionKey</span></span>
<span data-ttu-id="25a8d-121">A Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="25a8d-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="25a8d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25a8d-122">-InputObject</span></span>
<span data-ttu-id="25a8d-123">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="25a8d-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25a8d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="25a8d-124">-Name</span></span>
<span data-ttu-id="25a8d-125">A használni használt tárfiók neve</span><span class="sxs-lookup"><span data-stu-id="25a8d-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25a8d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25a8d-126">-ResourceGroupName</span></span>
<span data-ttu-id="25a8d-127">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="25a8d-127">Resource Group Name</span></span>

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

### <span data-ttu-id="25a8d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25a8d-128">-ResourceId</span></span>
<span data-ttu-id="25a8d-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="25a8d-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="25a8d-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="25a8d-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="25a8d-131">tárfiók hozzáférési kulcsának létrehozása</span><span class="sxs-lookup"><span data-stu-id="25a8d-131">provide storage account access key</span></span>

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

### <span data-ttu-id="25a8d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25a8d-132">-Confirm</span></span>
<span data-ttu-id="25a8d-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="25a8d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25a8d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25a8d-134">-WhatIf</span></span>
<span data-ttu-id="25a8d-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="25a8d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25a8d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25a8d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25a8d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a8d-137">CommonParameters</span></span>
<span data-ttu-id="25a8d-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25a8d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a8d-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25a8d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a8d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25a8d-140">INPUTS</span></span>

### <span data-ttu-id="25a8d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="25a8d-141">System.String</span></span>

### <span data-ttu-id="25a8d-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="25a8d-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="25a8d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25a8d-143">OUTPUTS</span></span>

### <span data-ttu-id="25a8d-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="25a8d-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="25a8d-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="25a8d-145">NOTES</span></span>

## <span data-ttu-id="25a8d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25a8d-146">RELATED LINKS</span></span>
