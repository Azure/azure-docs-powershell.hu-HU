---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: d7d2481173592adbb478a475730eb3c2db7e6f92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004310"
---
# <span data-ttu-id="69977-101">Remove-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="69977-101">Remove-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="69977-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69977-102">SYNOPSIS</span></span>
<span data-ttu-id="69977-103">Eltávolítja egy eszköz tárfiók-hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="69977-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="69977-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69977-104">SYNTAX</span></span>

### <span data-ttu-id="69977-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69977-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69977-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69977-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69977-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69977-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-InputObject] <PSDataBoxEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69977-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69977-108">DESCRIPTION</span></span>
<span data-ttu-id="69977-109">A **Remove-AzDataBoxEdgeStorageAccountCredential** parancsmag eltávolítja a tárfiók hitelesítő adatait egy Data Box Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="69977-109">The **Remove-AzDataBoxEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="69977-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69977-110">EXAMPLES</span></span>

### <span data-ttu-id="69977-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="69977-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="69977-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69977-112">PARAMETERS</span></span>

### <span data-ttu-id="69977-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69977-113">-AsJob</span></span>
<span data-ttu-id="69977-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="69977-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69977-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69977-115">-DefaultProfile</span></span>
<span data-ttu-id="69977-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69977-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69977-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="69977-117">-DeviceName</span></span>
<span data-ttu-id="69977-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="69977-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69977-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69977-119">-InputObject</span></span>
<span data-ttu-id="69977-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="69977-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69977-121">-Name</span><span class="sxs-lookup"><span data-stu-id="69977-121">-Name</span></span>
<span data-ttu-id="69977-122">A használni használt tárfiók neve</span><span class="sxs-lookup"><span data-stu-id="69977-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69977-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69977-123">-PassThru</span></span>
<span data-ttu-id="69977-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="69977-124">returns true if successful</span></span>

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

### <span data-ttu-id="69977-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69977-125">-ResourceGroupName</span></span>
<span data-ttu-id="69977-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="69977-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69977-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69977-127">-ResourceId</span></span>
<span data-ttu-id="69977-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="69977-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="69977-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69977-129">-Confirm</span></span>
<span data-ttu-id="69977-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="69977-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69977-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69977-131">-WhatIf</span></span>
<span data-ttu-id="69977-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="69977-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69977-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69977-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69977-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69977-134">CommonParameters</span></span>
<span data-ttu-id="69977-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69977-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69977-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69977-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69977-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69977-137">INPUTS</span></span>

### <span data-ttu-id="69977-138">System.String</span><span class="sxs-lookup"><span data-stu-id="69977-138">System.String</span></span>

### <span data-ttu-id="69977-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="69977-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="69977-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69977-140">OUTPUTS</span></span>

### <span data-ttu-id="69977-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69977-141">System.Boolean</span></span>

## <span data-ttu-id="69977-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69977-142">NOTES</span></span>

## <span data-ttu-id="69977-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69977-143">RELATED LINKS</span></span>
