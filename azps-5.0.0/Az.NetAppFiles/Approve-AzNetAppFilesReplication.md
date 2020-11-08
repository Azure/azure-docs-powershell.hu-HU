---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: 9afa4f22de142dba7608d33ed04c972758911aa9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194102"
---
# <span data-ttu-id="8c64a-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="8c64a-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="8c64a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c64a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c64a-103">Replikációs kapcsolat jóváhagyása/engedélyezése a forrás köteten</span><span class="sxs-lookup"><span data-stu-id="8c64a-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="8c64a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c64a-104">SYNTAX</span></span>

### <span data-ttu-id="8c64a-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c64a-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c64a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c64a-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c64a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c64a-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c64a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c64a-108">DESCRIPTION</span></span>
<span data-ttu-id="8c64a-109">A forrás köteten lévő replikációs kapcsolat jóváhagyása</span><span class="sxs-lookup"><span data-stu-id="8c64a-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="8c64a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8c64a-110">EXAMPLES</span></span>

### <span data-ttu-id="8c64a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8c64a-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="8c64a-112">Ez a parancs jóváhagyja a replikációt az MyAnfVolume-on.</span><span class="sxs-lookup"><span data-stu-id="8c64a-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="8c64a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c64a-113">PARAMETERS</span></span>

### <span data-ttu-id="8c64a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8c64a-114">-AccountName</span></span>
<span data-ttu-id="8c64a-115">A ANF-fiók neve a replikációs forrás kötetében</span><span class="sxs-lookup"><span data-stu-id="8c64a-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="8c64a-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="8c64a-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="8c64a-117">A cél adatvédelemi kötetének fájlrendszer-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8c64a-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="8c64a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c64a-118">-DefaultProfile</span></span>
<span data-ttu-id="8c64a-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c64a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c64a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c64a-120">-InputObject</span></span>
<span data-ttu-id="8c64a-121">A ANF objektum a replikációs cél engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="8c64a-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="8c64a-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8c64a-122">-Name</span></span>
<span data-ttu-id="8c64a-123">A ANF replikációs forrásának a neve</span><span class="sxs-lookup"><span data-stu-id="8c64a-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="8c64a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c64a-124">-PassThru</span></span>
<span data-ttu-id="8c64a-125">A megadott kötet replikációs engedélyezésének visszaadása</span><span class="sxs-lookup"><span data-stu-id="8c64a-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="8c64a-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8c64a-126">-PoolName</span></span>
<span data-ttu-id="8c64a-127">A ANF-készlet neve a replikációs forrás kötetében</span><span class="sxs-lookup"><span data-stu-id="8c64a-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="8c64a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c64a-128">-ResourceGroupName</span></span>
<span data-ttu-id="8c64a-129">A ANF replikációs forrásának erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="8c64a-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="8c64a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c64a-130">-ResourceId</span></span>
<span data-ttu-id="8c64a-131">A ANF replikációs forrásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8c64a-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="8c64a-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8c64a-132">-Confirm</span></span>
<span data-ttu-id="8c64a-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c64a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c64a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c64a-134">-WhatIf</span></span>
<span data-ttu-id="8c64a-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8c64a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c64a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c64a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c64a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c64a-137">CommonParameters</span></span>
<span data-ttu-id="8c64a-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c64a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c64a-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8c64a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c64a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c64a-140">INPUTS</span></span>

### <span data-ttu-id="8c64a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8c64a-141">System.String</span></span>

### <span data-ttu-id="8c64a-142">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8c64a-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8c64a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c64a-143">OUTPUTS</span></span>

### <span data-ttu-id="8c64a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8c64a-144">System.Boolean</span></span>

## <span data-ttu-id="8c64a-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c64a-145">NOTES</span></span>

## <span data-ttu-id="8c64a-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c64a-146">RELATED LINKS</span></span>
