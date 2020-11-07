---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: f6b21f3496f8ac05147db24de1df2ee03693fb7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670762"
---
# <span data-ttu-id="f15cb-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f15cb-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="f15cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f15cb-102">SYNOPSIS</span></span>
<span data-ttu-id="f15cb-103">Azure NetApp-fájlok (ANF-kötetek) törlése</span><span class="sxs-lookup"><span data-stu-id="f15cb-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="f15cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f15cb-104">SYNTAX</span></span>

### <span data-ttu-id="f15cb-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f15cb-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f15cb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f15cb-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f15cb-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f15cb-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f15cb-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f15cb-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f15cb-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f15cb-109">DESCRIPTION</span></span>
<span data-ttu-id="f15cb-110">A **Remove-AzNetAppFilesVolume** parancsmag ANF-kötetet töröl.</span><span class="sxs-lookup"><span data-stu-id="f15cb-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="f15cb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f15cb-111">EXAMPLES</span></span>

### <span data-ttu-id="f15cb-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f15cb-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="f15cb-113">Ez a parancs törli a "MyAnfVolume" ANF-kötetet.</span><span class="sxs-lookup"><span data-stu-id="f15cb-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="f15cb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f15cb-114">PARAMETERS</span></span>

### <span data-ttu-id="f15cb-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f15cb-115">-AccountName</span></span>
<span data-ttu-id="f15cb-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="f15cb-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f15cb-117">-DefaultProfile</span></span>
<span data-ttu-id="f15cb-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f15cb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15cb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f15cb-119">-InputObject</span></span>
<span data-ttu-id="f15cb-120">Eltávolítandó kötet objektum</span><span class="sxs-lookup"><span data-stu-id="f15cb-120">The volume object to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f15cb-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f15cb-121">-Name</span></span>
<span data-ttu-id="f15cb-122">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="f15cb-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15cb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f15cb-123">-PassThru</span></span>
<span data-ttu-id="f15cb-124">A megadott kötet sikeres eltávolításának visszaadása</span><span class="sxs-lookup"><span data-stu-id="f15cb-124">Return whether the specified volume was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15cb-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f15cb-125">-PoolName</span></span>
<span data-ttu-id="f15cb-126">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="f15cb-126">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15cb-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="f15cb-127">-PoolObject</span></span>
<span data-ttu-id="f15cb-128">Az eltávolítandó kötetet tartalmazó Pool objektum</span><span class="sxs-lookup"><span data-stu-id="f15cb-128">The pool object containing the volume to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f15cb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f15cb-129">-ResourceGroupName</span></span>
<span data-ttu-id="f15cb-130">A ANF-kötet erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="f15cb-130">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15cb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f15cb-131">-ResourceId</span></span>
<span data-ttu-id="f15cb-132">A ANF-kötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f15cb-132">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f15cb-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f15cb-133">-Confirm</span></span>
<span data-ttu-id="f15cb-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f15cb-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15cb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f15cb-135">-WhatIf</span></span>
<span data-ttu-id="f15cb-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f15cb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f15cb-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f15cb-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15cb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f15cb-138">CommonParameters</span></span>
<span data-ttu-id="f15cb-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f15cb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f15cb-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f15cb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f15cb-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f15cb-141">INPUTS</span></span>

### <span data-ttu-id="f15cb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f15cb-142">System.String</span></span>

### <span data-ttu-id="f15cb-143">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f15cb-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="f15cb-144">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f15cb-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f15cb-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f15cb-145">OUTPUTS</span></span>

### <span data-ttu-id="f15cb-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f15cb-146">System.Boolean</span></span>

## <span data-ttu-id="f15cb-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f15cb-147">NOTES</span></span>

## <span data-ttu-id="f15cb-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f15cb-148">RELATED LINKS</span></span>
