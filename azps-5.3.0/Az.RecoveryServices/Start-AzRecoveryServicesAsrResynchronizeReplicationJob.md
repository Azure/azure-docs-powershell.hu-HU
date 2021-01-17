---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0429976c64ed6e7989208c28fea1ee0a008436c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384396"
---
# <span data-ttu-id="ce64b-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="ce64b-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="ce64b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce64b-102">SYNOPSIS</span></span>
<span data-ttu-id="ce64b-103">Replikációs újraszinkronizálás indítása.</span><span class="sxs-lookup"><span data-stu-id="ce64b-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="ce64b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ce64b-104">SYNTAX</span></span>

### <span data-ttu-id="ce64b-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ce64b-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce64b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ce64b-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce64b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ce64b-107">DESCRIPTION</span></span>
<span data-ttu-id="ce64b-108">A **Start-AzRecoveryServicesAsrResynchronizeReplication Parancsmag** elindítja a megadott védett elem replikációs újraszinkronizálását, ha a védett elem újraszinkronizálási szükséges állapotban van.</span><span class="sxs-lookup"><span data-stu-id="ce64b-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="ce64b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ce64b-109">EXAMPLES</span></span>

### <span data-ttu-id="ce64b-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="ce64b-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="ce64b-111">Elindítja a replikációs újraszinkronizálási feladatot a több replikációval védett elemen.</span><span class="sxs-lookup"><span data-stu-id="ce64b-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="ce64b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce64b-112">PARAMETERS</span></span>

### <span data-ttu-id="ce64b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce64b-113">-DefaultProfile</span></span>
<span data-ttu-id="ce64b-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce64b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce64b-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ce64b-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ce64b-116">AsR replikációs védett elem a replikáció újraszinkronizálása érdekében.</span><span class="sxs-lookup"><span data-stu-id="ce64b-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce64b-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce64b-117">-ResourceId</span></span>
<span data-ttu-id="ce64b-118">Az újraszinkronizálni kívánt replikációs védett elem erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ce64b-118">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce64b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce64b-119">-Confirm</span></span>
<span data-ttu-id="ce64b-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ce64b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce64b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce64b-121">-WhatIf</span></span>
<span data-ttu-id="ce64b-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ce64b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce64b-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ce64b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce64b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce64b-124">CommonParameters</span></span>
<span data-ttu-id="ce64b-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce64b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce64b-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce64b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce64b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce64b-127">INPUTS</span></span>

### <span data-ttu-id="ce64b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ce64b-128">System.String</span></span>

### <span data-ttu-id="ce64b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ce64b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ce64b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce64b-130">OUTPUTS</span></span>

### <span data-ttu-id="ce64b-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="ce64b-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ce64b-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ce64b-132">NOTES</span></span>

## <span data-ttu-id="ce64b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce64b-133">RELATED LINKS</span></span>
