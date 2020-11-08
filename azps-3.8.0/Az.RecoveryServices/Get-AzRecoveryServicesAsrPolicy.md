---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a7cd359714be965c232019310ac2f2abfe0fe233
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010616"
---
# <span data-ttu-id="a2aa8-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="a2aa8-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="a2aa8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="a2aa8-103">ASR-replikációs házirendek jelentkeznek.</span><span class="sxs-lookup"><span data-stu-id="a2aa8-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="a2aa8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2aa8-104">SYNTAX</span></span>

### <span data-ttu-id="a2aa8-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2aa8-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2aa8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a2aa8-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2aa8-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a2aa8-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2aa8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2aa8-108">DESCRIPTION</span></span>
<span data-ttu-id="a2aa8-109">A **Get-AzRecoveryServicesAsrPolicy** parancsmag a konfigurált Azure-webhelyek helyreállítási replikációs házirendjeinek vagy egy adott replikációs házirendnek a neve alapján kapja meg a listát.</span><span class="sxs-lookup"><span data-stu-id="a2aa8-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="a2aa8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a2aa8-110">EXAMPLES</span></span>

### <span data-ttu-id="a2aa8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a2aa8-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="a2aa8-112">A replikációs házirendek listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="a2aa8-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="a2aa8-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="a2aa8-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="a2aa8-114">A név nevű replikációs házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a2aa8-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="a2aa8-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="a2aa8-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="a2aa8-116">A megadott felhasználóbarát névvel rendelkező replikációs házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a2aa8-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="a2aa8-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2aa8-117">PARAMETERS</span></span>

### <span data-ttu-id="a2aa8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2aa8-118">-DefaultProfile</span></span>
<span data-ttu-id="a2aa8-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2aa8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a2aa8-120">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="a2aa8-120">-FriendlyName</span></span>
<span data-ttu-id="a2aa8-121">Az ASR-replikációs házirend rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2aa8-121">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2aa8-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2aa8-122">-Name</span></span>
<span data-ttu-id="a2aa8-123">Az ASR-replikációs házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2aa8-123">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2aa8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2aa8-124">CommonParameters</span></span>
<span data-ttu-id="a2aa8-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2aa8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2aa8-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a2aa8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2aa8-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2aa8-127">INPUTS</span></span>

### <span data-ttu-id="a2aa8-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="a2aa8-128">None</span></span>

## <span data-ttu-id="a2aa8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2aa8-129">OUTPUTS</span></span>

### <span data-ttu-id="a2aa8-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="a2aa8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="a2aa8-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2aa8-131">NOTES</span></span>

## <span data-ttu-id="a2aa8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2aa8-132">RELATED LINKS</span></span>

[<span data-ttu-id="a2aa8-133">Új – AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="a2aa8-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="a2aa8-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="a2aa8-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
