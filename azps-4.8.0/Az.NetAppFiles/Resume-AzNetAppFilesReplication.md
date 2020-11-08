---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024668"
---
# <span data-ttu-id="b1f67-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="b1f67-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="b1f67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1f67-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f67-103">A cél köteten lévő kapcsolat folytatása és újraszinkronizálása.</span><span class="sxs-lookup"><span data-stu-id="b1f67-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="b1f67-104">Ha a művelet a forrás köteten futott, a program visszafordítja a kapcsolatot, majd szinkronizálja a forrástól a cél értékre.</span><span class="sxs-lookup"><span data-stu-id="b1f67-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="b1f67-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1f67-105">SYNTAX</span></span>

### <span data-ttu-id="b1f67-106">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b1f67-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1f67-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1f67-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1f67-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1f67-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1f67-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1f67-109">DESCRIPTION</span></span>
<span data-ttu-id="b1f67-110">A cél köteten lévő kapcsolat folytatása és újraszinkronizálása</span><span class="sxs-lookup"><span data-stu-id="b1f67-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="b1f67-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b1f67-111">EXAMPLES</span></span>

### <span data-ttu-id="b1f67-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b1f67-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="b1f67-113">Ez a parancs folytatja a ANF replikációs kapcsolatát a "MyDestinationAnfVolume" köteten.</span><span class="sxs-lookup"><span data-stu-id="b1f67-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="b1f67-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1f67-114">PARAMETERS</span></span>

### <span data-ttu-id="b1f67-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b1f67-115">-AccountName</span></span>
<span data-ttu-id="b1f67-116">A replikációs kötet ANF-fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="b1f67-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="b1f67-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f67-117">-DefaultProfile</span></span>
<span data-ttu-id="b1f67-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1f67-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1f67-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1f67-119">-InputObject</span></span>
<span data-ttu-id="b1f67-120">A ANF replikációs cél mennyiségi objektuma az újraszinkronizáláshoz</span><span class="sxs-lookup"><span data-stu-id="b1f67-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="b1f67-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b1f67-121">-Name</span></span>
<span data-ttu-id="b1f67-122">A ANF replikációs cél kötetének neve</span><span class="sxs-lookup"><span data-stu-id="b1f67-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="b1f67-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1f67-123">-PassThru</span></span>
<span data-ttu-id="b1f67-124">A megadott replikációs kötet újraszinkronizálásának visszaadása</span><span class="sxs-lookup"><span data-stu-id="b1f67-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="b1f67-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b1f67-125">-PoolName</span></span>
<span data-ttu-id="b1f67-126">A replikációs kötet ANF-készletének neve</span><span class="sxs-lookup"><span data-stu-id="b1f67-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="b1f67-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1f67-127">-ResourceGroupName</span></span>
<span data-ttu-id="b1f67-128">A ANF replikációs rendeltetési kötetének erőforráscsoport</span><span class="sxs-lookup"><span data-stu-id="b1f67-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="b1f67-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1f67-129">-ResourceId</span></span>
<span data-ttu-id="b1f67-130">A ANF replikációs célként megadott kötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b1f67-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="b1f67-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b1f67-131">-Confirm</span></span>
<span data-ttu-id="b1f67-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b1f67-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1f67-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1f67-133">-WhatIf</span></span>
<span data-ttu-id="b1f67-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b1f67-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1f67-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b1f67-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1f67-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f67-136">CommonParameters</span></span>
<span data-ttu-id="b1f67-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1f67-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f67-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b1f67-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f67-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1f67-139">INPUTS</span></span>

### <span data-ttu-id="b1f67-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b1f67-140">System.String</span></span>

### <span data-ttu-id="b1f67-141">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b1f67-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b1f67-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1f67-142">OUTPUTS</span></span>

### <span data-ttu-id="b1f67-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1f67-143">System.Boolean</span></span>

## <span data-ttu-id="b1f67-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1f67-144">NOTES</span></span>

## <span data-ttu-id="b1f67-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1f67-145">RELATED LINKS</span></span>
