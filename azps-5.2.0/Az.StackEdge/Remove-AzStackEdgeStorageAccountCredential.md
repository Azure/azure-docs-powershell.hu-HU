---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358706"
---
# <span data-ttu-id="e016d-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e016d-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="e016d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e016d-102">SYNOPSIS</span></span>
<span data-ttu-id="e016d-103">Eltávolítja egy eszköz tárfiók-hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="e016d-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="e016d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e016d-104">SYNTAX</span></span>

### <span data-ttu-id="e016d-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e016d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e016d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e016d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e016d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e016d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e016d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e016d-108">DESCRIPTION</span></span>
<span data-ttu-id="e016d-109">A **Remove-AzStackEdgeStorageAccountCredential** parancsmag eltávolítja a stack edge-es eszköz tárfiók-hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="e016d-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="e016d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e016d-110">EXAMPLES</span></span>

### <span data-ttu-id="e016d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e016d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="e016d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e016d-112">PARAMETERS</span></span>

### <span data-ttu-id="e016d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e016d-113">-AsJob</span></span>
<span data-ttu-id="e016d-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e016d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e016d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e016d-115">-DefaultProfile</span></span>
<span data-ttu-id="e016d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e016d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e016d-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e016d-117">-DeviceName</span></span>
<span data-ttu-id="e016d-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="e016d-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e016d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e016d-119">-InputObject</span></span>
<span data-ttu-id="e016d-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="e016d-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e016d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e016d-121">-Name</span></span>
<span data-ttu-id="e016d-122">A használni használt tárfiók neve</span><span class="sxs-lookup"><span data-stu-id="e016d-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e016d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e016d-123">-PassThru</span></span>
<span data-ttu-id="e016d-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="e016d-124">returns true if successful</span></span>

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

### <span data-ttu-id="e016d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e016d-125">-ResourceGroupName</span></span>
<span data-ttu-id="e016d-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e016d-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e016d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e016d-127">-ResourceId</span></span>
<span data-ttu-id="e016d-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e016d-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e016d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e016d-129">-Confirm</span></span>
<span data-ttu-id="e016d-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e016d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e016d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e016d-131">-WhatIf</span></span>
<span data-ttu-id="e016d-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e016d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e016d-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e016d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e016d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e016d-134">CommonParameters</span></span>
<span data-ttu-id="e016d-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e016d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e016d-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e016d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e016d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e016d-137">INPUTS</span></span>

### <span data-ttu-id="e016d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e016d-138">System.String</span></span>

### <span data-ttu-id="e016d-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e016d-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="e016d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e016d-140">OUTPUTS</span></span>

### <span data-ttu-id="e016d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e016d-141">System.Boolean</span></span>

## <span data-ttu-id="e016d-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e016d-142">NOTES</span></span>

## <span data-ttu-id="e016d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e016d-143">RELATED LINKS</span></span>
