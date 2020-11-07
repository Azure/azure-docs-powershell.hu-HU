---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d5b7965ed6dea106a40a6be07171e9a3c258f5d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672403"
---
# <span data-ttu-id="8ef6d-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8ef6d-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="8ef6d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ef6d-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef6d-103">Webhely-helyreállítási csomag szerkesztése</span><span class="sxs-lookup"><span data-stu-id="8ef6d-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ef6d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ef6d-104">SYNTAX</span></span>

### <span data-ttu-id="8ef6d-105">AppendGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ef6d-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ef6d-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="8ef6d-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ef6d-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="8ef6d-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ef6d-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="8ef6d-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ef6d-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="8ef6d-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ef6d-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="8ef6d-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ef6d-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ef6d-111">DESCRIPTION</span></span>
<span data-ttu-id="8ef6d-112">A **Edit-AzureRmSiteRecoveryRecoveryPlan** parancsmag az Azure-webhely helyreállítási csomagját szerkeszti.</span><span class="sxs-lookup"><span data-stu-id="8ef6d-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="8ef6d-113">Példák</span><span class="sxs-lookup"><span data-stu-id="8ef6d-113">EXAMPLES</span></span>

## <span data-ttu-id="8ef6d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ef6d-114">PARAMETERS</span></span>

### <span data-ttu-id="8ef6d-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="8ef6d-115">-AddProtectedEntities</span></span>
<span data-ttu-id="8ef6d-116">A felvenni kívánt védett entitások tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ef6d-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ef6d-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="8ef6d-117">-AddProtectedItems</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ef6d-118">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="8ef6d-118">-AppendGroup</span></span>
<span data-ttu-id="8ef6d-119">Azt jelzi, hogy ez a művelet hozzáfűzi a csoportot a helyreállítási terv objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="8ef6d-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ef6d-120">-Csoport</span><span class="sxs-lookup"><span data-stu-id="8ef6d-120">-Group</span></span>
<span data-ttu-id="8ef6d-121">A webhely-helyreállítási terv csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ef6d-121">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ef6d-122">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8ef6d-122">-RecoveryPlan</span></span>
<span data-ttu-id="8ef6d-123">Helyreállítási tervet ad meg.</span><span class="sxs-lookup"><span data-stu-id="8ef6d-123">Specifies a recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ef6d-124">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="8ef6d-124">-RemoveGroup</span></span>
<span data-ttu-id="8ef6d-125">Eltávolítja a megadott webhelycsoport-helyreállítási terv csoportot.</span><span class="sxs-lookup"><span data-stu-id="8ef6d-125">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ef6d-126">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="8ef6d-126">-RemoveProtectedEntities</span></span>
<span data-ttu-id="8ef6d-127">A védett entitások tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ef6d-127">Specifies an array of protected entities.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ef6d-128">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="8ef6d-128">-RemoveProtectedItems</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ef6d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ef6d-129">-DefaultProfile</span></span>
<span data-ttu-id="8ef6d-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ef6d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ef6d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef6d-131">CommonParameters</span></span>
<span data-ttu-id="8ef6d-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ef6d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef6d-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ef6d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef6d-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ef6d-134">INPUTS</span></span>

### <span data-ttu-id="8ef6d-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8ef6d-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="8ef6d-136">A ' RecoveryPlan ' paraméter az "ASRRecoveryPlan" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8ef6d-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="8ef6d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ef6d-137">OUTPUTS</span></span>

## <span data-ttu-id="8ef6d-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ef6d-138">NOTES</span></span>

## <span data-ttu-id="8ef6d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ef6d-139">RELATED LINKS</span></span>

[<span data-ttu-id="8ef6d-140">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8ef6d-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="8ef6d-141">Új – AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8ef6d-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)
