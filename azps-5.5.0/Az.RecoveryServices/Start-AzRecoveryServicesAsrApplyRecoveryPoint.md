---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 893298c3349d2d7ceaa998a1f147ce8dd590f101
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158514"
---
# <span data-ttu-id="9e58e-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9e58e-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="9e58e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e58e-102">SYNOPSIS</span></span>
<span data-ttu-id="9e58e-103">A feladatátvételi művelet végrehajtása előtt módosít egy helyreállítási pontot egy sikertelenül védett elemhez.</span><span class="sxs-lookup"><span data-stu-id="9e58e-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="9e58e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9e58e-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e58e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9e58e-105">DESCRIPTION</span></span>
<span data-ttu-id="9e58e-106">A **Start-AzRecoveryServicesAsrApplyRecoveryPoint** a feladatátvételi művelet végrehajtása előtt módosítja egy sikertelenül védett elem helyreállítási pontját.</span><span class="sxs-lookup"><span data-stu-id="9e58e-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="9e58e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9e58e-107">EXAMPLES</span></span>

### <span data-ttu-id="9e58e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9e58e-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="9e58e-109">Megkezdi a megadott helyreállítási pont alkalmazását a replikációval védett elemre, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="9e58e-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9e58e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e58e-110">PARAMETERS</span></span>

### <span data-ttu-id="9e58e-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="9e58e-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="9e58e-112">Az elsődleges tanúsítványfájl megadása adattitkosítás használata esetén.</span><span class="sxs-lookup"><span data-stu-id="9e58e-112">Specifies the primary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e58e-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="9e58e-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="9e58e-114">A másodlagos tanúsítványfájl megadása adattitkosítás használata esetén.</span><span class="sxs-lookup"><span data-stu-id="9e58e-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e58e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e58e-115">-DefaultProfile</span></span>
<span data-ttu-id="9e58e-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e58e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9e58e-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9e58e-117">-RecoveryPoint</span></span>
<span data-ttu-id="9e58e-118">Az alkalmazandó helyreállítási pontnak megfelelő helyreállításipont-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e58e-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e58e-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9e58e-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9e58e-120">Az ASR replikációs védelem alatt ható elemobjektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e58e-120">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e58e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e58e-121">-Confirm</span></span>
<span data-ttu-id="9e58e-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9e58e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e58e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e58e-123">-WhatIf</span></span>
<span data-ttu-id="9e58e-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9e58e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e58e-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e58e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e58e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e58e-126">CommonParameters</span></span>
<span data-ttu-id="9e58e-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e58e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e58e-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e58e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e58e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e58e-129">INPUTS</span></span>

### <span data-ttu-id="9e58e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9e58e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9e58e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e58e-131">OUTPUTS</span></span>

### <span data-ttu-id="9e58e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="9e58e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9e58e-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9e58e-133">NOTES</span></span>

## <span data-ttu-id="9e58e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e58e-134">RELATED LINKS</span></span>

[<span data-ttu-id="9e58e-135">Azure-webhely-helyreállítási parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9e58e-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)
