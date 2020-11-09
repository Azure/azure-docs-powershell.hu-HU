---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: eb695da1dc1fea238a57ea1c98bec42899e8f28f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303168"
---
# <span data-ttu-id="34f83-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="34f83-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="34f83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34f83-102">SYNOPSIS</span></span>
<span data-ttu-id="34f83-103">A replikációs kapcsolat felfüggesztése/megszüntetése a célként megadott köteten</span><span class="sxs-lookup"><span data-stu-id="34f83-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="34f83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34f83-104">SYNTAX</span></span>

### <span data-ttu-id="34f83-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="34f83-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34f83-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34f83-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34f83-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34f83-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34f83-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="34f83-108">DESCRIPTION</span></span>
<span data-ttu-id="34f83-109">A replikációs kapcsolat felfüggesztése/megszüntetése a célként megadott köteten</span><span class="sxs-lookup"><span data-stu-id="34f83-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="34f83-110">Példák</span><span class="sxs-lookup"><span data-stu-id="34f83-110">EXAMPLES</span></span>

### <span data-ttu-id="34f83-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="34f83-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="34f83-112">Ez a parancs felfüggeszti a ANF replikációs kapcsolatát a "MyDestinationAnfVolume" köteten.</span><span class="sxs-lookup"><span data-stu-id="34f83-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="34f83-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34f83-113">PARAMETERS</span></span>

### <span data-ttu-id="34f83-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="34f83-114">-AccountName</span></span>
<span data-ttu-id="34f83-115">A replikációs kötet ANF-fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="34f83-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="34f83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f83-116">-DefaultProfile</span></span>
<span data-ttu-id="34f83-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="34f83-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34f83-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34f83-118">-InputObject</span></span>
<span data-ttu-id="34f83-119">A cél ANF objektum a replikációval</span><span class="sxs-lookup"><span data-stu-id="34f83-119">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="34f83-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="34f83-120">-Name</span></span>
<span data-ttu-id="34f83-121">A ANF replikációs cél kötetének neve</span><span class="sxs-lookup"><span data-stu-id="34f83-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f83-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34f83-122">-PassThru</span></span>
<span data-ttu-id="34f83-123">Annak megadása, hogy a megadott kötet-replikáció megszakítása történt-e</span><span class="sxs-lookup"><span data-stu-id="34f83-123">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="34f83-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="34f83-124">-PoolName</span></span>
<span data-ttu-id="34f83-125">A replikációs kötet ANF-készletének neve</span><span class="sxs-lookup"><span data-stu-id="34f83-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="34f83-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34f83-126">-ResourceGroupName</span></span>
<span data-ttu-id="34f83-127">A ANF replikációs rendeltetési kötetének erőforráscsoport</span><span class="sxs-lookup"><span data-stu-id="34f83-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="34f83-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34f83-128">-ResourceId</span></span>
<span data-ttu-id="34f83-129">A ANF replikációs célként megadott kötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="34f83-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="34f83-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="34f83-130">-Confirm</span></span>
<span data-ttu-id="34f83-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="34f83-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34f83-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34f83-132">-WhatIf</span></span>
<span data-ttu-id="34f83-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="34f83-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34f83-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="34f83-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34f83-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f83-135">CommonParameters</span></span>
<span data-ttu-id="34f83-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="34f83-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f83-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="34f83-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f83-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34f83-138">INPUTS</span></span>

### <span data-ttu-id="34f83-139">System. String</span><span class="sxs-lookup"><span data-stu-id="34f83-139">System.String</span></span>

### <span data-ttu-id="34f83-140">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="34f83-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="34f83-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34f83-141">OUTPUTS</span></span>

### <span data-ttu-id="34f83-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34f83-142">System.Boolean</span></span>

## <span data-ttu-id="34f83-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34f83-143">NOTES</span></span>

## <span data-ttu-id="34f83-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34f83-144">RELATED LINKS</span></span>
