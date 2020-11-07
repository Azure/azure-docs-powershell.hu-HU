---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: fa308c0961d11320964d7c31a7d77642e968b09b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679027"
---
# <span data-ttu-id="9cb5f-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9cb5f-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="9cb5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9cb5f-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb5f-103">Webhely-helyreállítási csomagot hoz létre a webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="9cb5f-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cb5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9cb5f-104">SYNTAX</span></span>

### <span data-ttu-id="9cb5f-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9cb5f-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9cb5f-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="9cb5f-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cb5f-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="9cb5f-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cb5f-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="9cb5f-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cb5f-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="9cb5f-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cb5f-110">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="9cb5f-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cb5f-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="9cb5f-111">DESCRIPTION</span></span>
<span data-ttu-id="9cb5f-112">A **New-AzureRmSiteRecoveryRecoveryPlan** parancsmag létrehoz egy helyreállítási tervet az Azure webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="9cb5f-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="9cb5f-113">A helyreállítási terv a virtuális gépeket egy csoportba gyűjti a feladatátvétel és helyreállítás céljából.</span><span class="sxs-lookup"><span data-stu-id="9cb5f-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="9cb5f-114">Példák</span><span class="sxs-lookup"><span data-stu-id="9cb5f-114">EXAMPLES</span></span>

### <span data-ttu-id="9cb5f-115">1. példa: helyreállítási terv hozzáadása a webhely-helyreállítási boltozathoz</span><span class="sxs-lookup"><span data-stu-id="9cb5f-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="9cb5f-116">Ez a parancs hozzáadja a RecoveryPlan.xml nevű helyreállítási csomagot az Azure-webhely helyreállítási boltozatához.</span><span class="sxs-lookup"><span data-stu-id="9cb5f-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="9cb5f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9cb5f-117">PARAMETERS</span></span>

### <span data-ttu-id="9cb5f-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="9cb5f-118">-Azure</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb5f-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="9cb5f-119">-FailoverDeploymentModel</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb5f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9cb5f-120">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb5f-121">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="9cb5f-121">-Path</span></span>
<span data-ttu-id="9cb5f-122">A helyreállítási terv fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cb5f-122">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb5f-123">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="9cb5f-123">-PrimaryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb5f-124">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="9cb5f-124">-PrimaryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb5f-125">-PrimarySite</span><span class="sxs-lookup"><span data-stu-id="9cb5f-125">-PrimarySite</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb5f-126">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="9cb5f-126">-ProtectionEntityList</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb5f-127">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="9cb5f-127">-RecoveryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb5f-128">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="9cb5f-128">-RecoveryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb5f-129">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9cb5f-129">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb5f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb5f-130">-DefaultProfile</span></span>
<span data-ttu-id="9cb5f-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cb5f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cb5f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb5f-132">CommonParameters</span></span>
<span data-ttu-id="9cb5f-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9cb5f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb5f-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cb5f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb5f-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cb5f-135">INPUTS</span></span>

### <span data-ttu-id="9cb5f-136">ASRProtectionEntity[]</span><span class="sxs-lookup"><span data-stu-id="9cb5f-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="9cb5f-137">A "ProtectionEntityList" paraméter az "ASRProtectionEntity []" típusú értéket adja meg a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9cb5f-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="9cb5f-138">ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="9cb5f-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="9cb5f-139">A "ReplicationProtectedItem" paraméter az "ASRReplicationProtectedItem []" típusú értéket adja meg a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9cb5f-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="9cb5f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cb5f-140">OUTPUTS</span></span>

## <span data-ttu-id="9cb5f-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9cb5f-141">NOTES</span></span>

## <span data-ttu-id="9cb5f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cb5f-142">RELATED LINKS</span></span>

[<span data-ttu-id="9cb5f-143">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9cb5f-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="9cb5f-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9cb5f-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="9cb5f-145">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9cb5f-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


