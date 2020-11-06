---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8aba5d85e11a6494c4362de4d729c5e7b64106fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502372"
---
# <span data-ttu-id="4ec20-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4ec20-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="4ec20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ec20-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec20-103">Webhely-helyreállítási csomagot hoz létre a webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="4ec20-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ec20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ec20-104">SYNTAX</span></span>

### <span data-ttu-id="4ec20-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ec20-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ec20-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="4ec20-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ec20-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="4ec20-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ec20-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="4ec20-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ec20-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="4ec20-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ec20-110">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="4ec20-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ec20-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ec20-111">DESCRIPTION</span></span>
<span data-ttu-id="4ec20-112">A **New-AzureRmSiteRecoveryRecoveryPlan** parancsmag létrehoz egy helyreállítási tervet az Azure webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="4ec20-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="4ec20-113">A helyreállítási terv a virtuális gépeket egy csoportba gyűjti a feladatátvétel és helyreállítás céljából.</span><span class="sxs-lookup"><span data-stu-id="4ec20-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="4ec20-114">Példák</span><span class="sxs-lookup"><span data-stu-id="4ec20-114">EXAMPLES</span></span>

### <span data-ttu-id="4ec20-115">1. példa: helyreállítási terv hozzáadása a webhely-helyreállítási boltozathoz</span><span class="sxs-lookup"><span data-stu-id="4ec20-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="4ec20-116">Ez a parancs hozzáadja a RecoveryPlan.xml nevű helyreállítási csomagot az Azure-webhely helyreállítási boltozatához.</span><span class="sxs-lookup"><span data-stu-id="4ec20-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="4ec20-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ec20-117">PARAMETERS</span></span>

### <span data-ttu-id="4ec20-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="4ec20-118">-Azure</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec20-119">-DefaultProfile</span></span>
<span data-ttu-id="4ec20-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ec20-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec20-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="4ec20-121">-FailoverDeploymentModel</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec20-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ec20-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec20-123">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="4ec20-123">-Path</span></span>
<span data-ttu-id="4ec20-124">A helyreállítási terv fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ec20-124">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec20-125">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="4ec20-125">-PrimaryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec20-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="4ec20-126">-PrimaryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec20-127">-PrimarySite</span><span class="sxs-lookup"><span data-stu-id="4ec20-127">-PrimarySite</span></span>
```yaml
Type: ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec20-128">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="4ec20-128">-ProtectionEntityList</span></span>
```yaml
Type: ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec20-129">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="4ec20-129">-RecoveryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec20-130">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="4ec20-130">-RecoveryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec20-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4ec20-131">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec20-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec20-132">CommonParameters</span></span>
<span data-ttu-id="4ec20-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ec20-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec20-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ec20-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec20-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ec20-135">INPUTS</span></span>

### <span data-ttu-id="4ec20-136">ASRProtectionEntity[]</span><span class="sxs-lookup"><span data-stu-id="4ec20-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="4ec20-137">A "ProtectionEntityList" paraméter az "ASRProtectionEntity []" típusú értéket adja meg a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4ec20-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="4ec20-138">ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="4ec20-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="4ec20-139">A "ReplicationProtectedItem" paraméter az "ASRReplicationProtectedItem []" típusú értéket adja meg a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4ec20-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="4ec20-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ec20-140">OUTPUTS</span></span>

## <span data-ttu-id="4ec20-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ec20-141">NOTES</span></span>

## <span data-ttu-id="4ec20-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ec20-142">RELATED LINKS</span></span>

[<span data-ttu-id="4ec20-143">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4ec20-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4ec20-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4ec20-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4ec20-145">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4ec20-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


