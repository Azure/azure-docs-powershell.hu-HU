---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303180"
---
# <span data-ttu-id="ec3ba-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="ec3ba-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="ec3ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ec3ba-103">A cél köteten lévő replikációs kapcsolat eltávolítása/törlése, és a kiadás küldése a forrás replikálásának</span><span class="sxs-lookup"><span data-stu-id="ec3ba-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="ec3ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec3ba-104">SYNTAX</span></span>

### <span data-ttu-id="ec3ba-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec3ba-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec3ba-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec3ba-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec3ba-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec3ba-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec3ba-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec3ba-108">DESCRIPTION</span></span>
<span data-ttu-id="ec3ba-109">A cél köteten lévő replikációs kapcsolat eltávolítása/törlése, és a kiadás küldése a forrás replikálásának</span><span class="sxs-lookup"><span data-stu-id="ec3ba-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="ec3ba-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ec3ba-110">EXAMPLES</span></span>

### <span data-ttu-id="ec3ba-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ec3ba-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="ec3ba-112">Ez a parancs eltávolítja a ANF replikációs kapcsolatát a "MyDestinationAnfVolume" köteten.</span><span class="sxs-lookup"><span data-stu-id="ec3ba-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="ec3ba-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec3ba-113">PARAMETERS</span></span>

### <span data-ttu-id="ec3ba-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ec3ba-114">-AccountName</span></span>
<span data-ttu-id="ec3ba-115">A replikációs kötet ANF-fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="ec3ba-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="ec3ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec3ba-116">-DefaultProfile</span></span>
<span data-ttu-id="ec3ba-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec3ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec3ba-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec3ba-118">-InputObject</span></span>
<span data-ttu-id="ec3ba-119">A ANF az eltávolítandó replikációval</span><span class="sxs-lookup"><span data-stu-id="ec3ba-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="ec3ba-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ec3ba-120">-Name</span></span>
<span data-ttu-id="ec3ba-121">A ANF replikációs cél kötetének neve</span><span class="sxs-lookup"><span data-stu-id="ec3ba-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ec3ba-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec3ba-122">-PassThru</span></span>
<span data-ttu-id="ec3ba-123">A megadott ANF-replikáció sikeres eltávolításának visszaadása</span><span class="sxs-lookup"><span data-stu-id="ec3ba-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="ec3ba-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ec3ba-124">-PoolName</span></span>
<span data-ttu-id="ec3ba-125">A replikációs kötet ANF-készletének neve</span><span class="sxs-lookup"><span data-stu-id="ec3ba-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="ec3ba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec3ba-126">-ResourceGroupName</span></span>
<span data-ttu-id="ec3ba-127">A ANF replikációs rendeltetési kötetének erőforráscsoport</span><span class="sxs-lookup"><span data-stu-id="ec3ba-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ec3ba-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec3ba-128">-ResourceId</span></span>
<span data-ttu-id="ec3ba-129">A ANF replikációs célként megadott kötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ec3ba-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ec3ba-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ec3ba-130">-Confirm</span></span>
<span data-ttu-id="ec3ba-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec3ba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec3ba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec3ba-132">-WhatIf</span></span>
<span data-ttu-id="ec3ba-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ec3ba-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec3ba-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec3ba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec3ba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec3ba-135">CommonParameters</span></span>
<span data-ttu-id="ec3ba-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec3ba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec3ba-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ec3ba-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec3ba-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec3ba-138">INPUTS</span></span>

### <span data-ttu-id="ec3ba-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ec3ba-139">System.String</span></span>

### <span data-ttu-id="ec3ba-140">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ec3ba-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ec3ba-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec3ba-141">OUTPUTS</span></span>

### <span data-ttu-id="ec3ba-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec3ba-142">System.Boolean</span></span>

## <span data-ttu-id="ec3ba-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec3ba-143">NOTES</span></span>

## <span data-ttu-id="ec3ba-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec3ba-144">RELATED LINKS</span></span>
