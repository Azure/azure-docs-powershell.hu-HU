---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 1f8e20b826a477778de5325ff147cbd7ad28a9fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345954"
---
# <span data-ttu-id="b380e-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b380e-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="b380e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b380e-102">SYNOPSIS</span></span>
<span data-ttu-id="b380e-103">Eltávolítja egy eszköz Edge Storage-fiókját.</span><span class="sxs-lookup"><span data-stu-id="b380e-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="b380e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b380e-104">SYNTAX</span></span>

### <span data-ttu-id="b380e-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b380e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b380e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b380e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b380e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b380e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b380e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b380e-108">DESCRIPTION</span></span>
<span data-ttu-id="b380e-109">A **Remove-AzDataBoxEdgeStorageAccount** parancsmag eltávolítja a kapcsolódó Edge Storage-fiókot egy Adatmező Edge-eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="b380e-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="b380e-110">Megadhatja a parancsmagban paraméterként eltávolítható Edge Storage-fiók nevét.</span><span class="sxs-lookup"><span data-stu-id="b380e-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="b380e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b380e-111">EXAMPLES</span></span>

### <span data-ttu-id="b380e-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="b380e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="b380e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b380e-113">PARAMETERS</span></span>

### <span data-ttu-id="b380e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b380e-114">-AsJob</span></span>
<span data-ttu-id="b380e-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b380e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b380e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b380e-116">-DefaultProfile</span></span>
<span data-ttu-id="b380e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b380e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b380e-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b380e-118">-DeviceName</span></span>
<span data-ttu-id="b380e-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="b380e-119">Device Name</span></span>

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

### <span data-ttu-id="b380e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b380e-120">-InputObject</span></span>
<span data-ttu-id="b380e-121">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="b380e-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b380e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b380e-122">-Name</span></span>
<span data-ttu-id="b380e-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="b380e-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b380e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b380e-124">-PassThru</span></span>
<span data-ttu-id="b380e-125">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="b380e-125">returns true if successful</span></span>

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

### <span data-ttu-id="b380e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b380e-126">-ResourceGroupName</span></span>
<span data-ttu-id="b380e-127">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b380e-127">Resource Group Name</span></span>

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

### <span data-ttu-id="b380e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b380e-128">-ResourceId</span></span>
<span data-ttu-id="b380e-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b380e-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="b380e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b380e-130">-Confirm</span></span>
<span data-ttu-id="b380e-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b380e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b380e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b380e-132">-WhatIf</span></span>
<span data-ttu-id="b380e-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b380e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b380e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b380e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b380e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b380e-135">CommonParameters</span></span>
<span data-ttu-id="b380e-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b380e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b380e-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b380e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b380e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b380e-138">INPUTS</span></span>

### <span data-ttu-id="b380e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b380e-139">System.String</span></span>

### <span data-ttu-id="b380e-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b380e-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="b380e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b380e-141">OUTPUTS</span></span>

### <span data-ttu-id="b380e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b380e-142">System.Boolean</span></span>

## <span data-ttu-id="b380e-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b380e-143">NOTES</span></span>

## <span data-ttu-id="b380e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b380e-144">RELATED LINKS</span></span>
