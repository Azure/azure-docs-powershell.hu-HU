---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194096"
---
# <span data-ttu-id="eb0e7-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="eb0e7-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="eb0e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb0e7-102">SYNOPSIS</span></span>
<span data-ttu-id="eb0e7-103">Azure NetApp-fájlok (ANF-kötetek) törlése</span><span class="sxs-lookup"><span data-stu-id="eb0e7-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="eb0e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb0e7-104">SYNTAX</span></span>

### <span data-ttu-id="eb0e7-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb0e7-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb0e7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb0e7-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb0e7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb0e7-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb0e7-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb0e7-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb0e7-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb0e7-109">DESCRIPTION</span></span>
<span data-ttu-id="eb0e7-110">A **Remove-AzNetAppFilesVolume** parancsmag ANF-kötetet töröl.</span><span class="sxs-lookup"><span data-stu-id="eb0e7-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="eb0e7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="eb0e7-111">EXAMPLES</span></span>

### <span data-ttu-id="eb0e7-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eb0e7-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="eb0e7-113">Ez a parancs törli a "MyAnfVolume" ANF-kötetet.</span><span class="sxs-lookup"><span data-stu-id="eb0e7-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="eb0e7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb0e7-114">PARAMETERS</span></span>

### <span data-ttu-id="eb0e7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eb0e7-115">-AccountName</span></span>
<span data-ttu-id="eb0e7-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="eb0e7-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb0e7-117">-DefaultProfile</span></span>
<span data-ttu-id="eb0e7-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb0e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb0e7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb0e7-119">-InputObject</span></span>
<span data-ttu-id="eb0e7-120">Eltávolítandó kötet objektum</span><span class="sxs-lookup"><span data-stu-id="eb0e7-120">The volume object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e7-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb0e7-121">-Name</span></span>
<span data-ttu-id="eb0e7-122">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="eb0e7-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb0e7-123">-PassThru</span></span>
<span data-ttu-id="eb0e7-124">A megadott kötet sikeres eltávolításának visszaadása</span><span class="sxs-lookup"><span data-stu-id="eb0e7-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="eb0e7-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="eb0e7-125">-PoolName</span></span>
<span data-ttu-id="eb0e7-126">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="eb0e7-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e7-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="eb0e7-127">-PoolObject</span></span>
<span data-ttu-id="eb0e7-128">Az eltávolítandó kötetet tartalmazó Pool objektum</span><span class="sxs-lookup"><span data-stu-id="eb0e7-128">The pool object containing the volume to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb0e7-129">-ResourceGroupName</span></span>
<span data-ttu-id="eb0e7-130">A ANF-kötet erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="eb0e7-130">The resource group of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb0e7-131">-ResourceId</span></span>
<span data-ttu-id="eb0e7-132">A ANF-kötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="eb0e7-132">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e7-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eb0e7-133">-Confirm</span></span>
<span data-ttu-id="eb0e7-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb0e7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb0e7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb0e7-135">-WhatIf</span></span>
<span data-ttu-id="eb0e7-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eb0e7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb0e7-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb0e7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb0e7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb0e7-138">CommonParameters</span></span>
<span data-ttu-id="eb0e7-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb0e7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb0e7-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eb0e7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb0e7-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb0e7-141">INPUTS</span></span>

### <span data-ttu-id="eb0e7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="eb0e7-142">System.String</span></span>

### <span data-ttu-id="eb0e7-143">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="eb0e7-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="eb0e7-144">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="eb0e7-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="eb0e7-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb0e7-145">OUTPUTS</span></span>

### <span data-ttu-id="eb0e7-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb0e7-146">System.Boolean</span></span>

## <span data-ttu-id="eb0e7-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb0e7-147">NOTES</span></span>

## <span data-ttu-id="eb0e7-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb0e7-148">RELATED LINKS</span></span>