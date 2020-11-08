---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181622"
---
# <span data-ttu-id="91241-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="91241-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="91241-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91241-102">SYNOPSIS</span></span>
<span data-ttu-id="91241-103">A cél köteten lévő replikációs kapcsolat eltávolítása/törlése, és a kiadás küldése a forrás replikálásának</span><span class="sxs-lookup"><span data-stu-id="91241-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="91241-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91241-104">SYNTAX</span></span>

### <span data-ttu-id="91241-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91241-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91241-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91241-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91241-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91241-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91241-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="91241-108">DESCRIPTION</span></span>
<span data-ttu-id="91241-109">A cél köteten lévő replikációs kapcsolat eltávolítása/törlése, és a kiadás küldése a forrás replikálásának</span><span class="sxs-lookup"><span data-stu-id="91241-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="91241-110">Példák</span><span class="sxs-lookup"><span data-stu-id="91241-110">EXAMPLES</span></span>

### <span data-ttu-id="91241-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="91241-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="91241-112">Ez a parancs eltávolítja a ANF replikációs kapcsolatát a "MyDestinationAnfVolume" köteten.</span><span class="sxs-lookup"><span data-stu-id="91241-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="91241-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91241-113">PARAMETERS</span></span>

### <span data-ttu-id="91241-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="91241-114">-AccountName</span></span>
<span data-ttu-id="91241-115">A replikációs kötet ANF-fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="91241-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="91241-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91241-116">-DefaultProfile</span></span>
<span data-ttu-id="91241-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91241-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91241-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91241-118">-InputObject</span></span>
<span data-ttu-id="91241-119">A ANF az eltávolítandó replikációval</span><span class="sxs-lookup"><span data-stu-id="91241-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="91241-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91241-120">-Name</span></span>
<span data-ttu-id="91241-121">A ANF replikációs cél kötetének neve</span><span class="sxs-lookup"><span data-stu-id="91241-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="91241-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91241-122">-PassThru</span></span>
<span data-ttu-id="91241-123">A megadott ANF-replikáció sikeres eltávolításának visszaadása</span><span class="sxs-lookup"><span data-stu-id="91241-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="91241-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="91241-124">-PoolName</span></span>
<span data-ttu-id="91241-125">A replikációs kötet ANF-készletének neve</span><span class="sxs-lookup"><span data-stu-id="91241-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="91241-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91241-126">-ResourceGroupName</span></span>
<span data-ttu-id="91241-127">A ANF replikációs rendeltetési kötetének erőforráscsoport</span><span class="sxs-lookup"><span data-stu-id="91241-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="91241-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91241-128">-ResourceId</span></span>
<span data-ttu-id="91241-129">A ANF replikációs célként megadott kötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="91241-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="91241-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="91241-130">-Confirm</span></span>
<span data-ttu-id="91241-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="91241-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91241-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91241-132">-WhatIf</span></span>
<span data-ttu-id="91241-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="91241-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91241-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91241-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91241-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91241-135">CommonParameters</span></span>
<span data-ttu-id="91241-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91241-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91241-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="91241-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91241-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91241-138">INPUTS</span></span>

### <span data-ttu-id="91241-139">System. String</span><span class="sxs-lookup"><span data-stu-id="91241-139">System.String</span></span>

### <span data-ttu-id="91241-140">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="91241-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="91241-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91241-141">OUTPUTS</span></span>

### <span data-ttu-id="91241-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91241-142">System.Boolean</span></span>

## <span data-ttu-id="91241-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91241-143">NOTES</span></span>

## <span data-ttu-id="91241-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91241-144">RELATED LINKS</span></span>
