---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a7cd359714be965c232019310ac2f2abfe0fe233
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169290"
---
# <span data-ttu-id="bcb1c-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="bcb1c-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="bcb1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcb1c-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb1c-103">AsR replikációs házirendeket kap.</span><span class="sxs-lookup"><span data-stu-id="bcb1c-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="bcb1c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bcb1c-104">SYNTAX</span></span>

### <span data-ttu-id="bcb1c-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bcb1c-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcb1c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bcb1c-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcb1c-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="bcb1c-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcb1c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bcb1c-108">DESCRIPTION</span></span>
<span data-ttu-id="bcb1c-109">A **Get-AzRecoveryServicesAsrPolicy** parancsmag lekérte a konfigurált Azure-webhely-helyreállítási replikációs házirendek vagy név szerint meghatározott replikációs házirendek listáját.</span><span class="sxs-lookup"><span data-stu-id="bcb1c-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="bcb1c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bcb1c-110">EXAMPLES</span></span>

### <span data-ttu-id="bcb1c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="bcb1c-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="bcb1c-112">A replikációs házirendek listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="bcb1c-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="bcb1c-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="bcb1c-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="bcb1c-114">Névvel megadott replikációs házirendet ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="bcb1c-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="bcb1c-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="bcb1c-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="bcb1c-116">A megadott rövid névvel megadott replikációs házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="bcb1c-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="bcb1c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcb1c-117">PARAMETERS</span></span>

### <span data-ttu-id="bcb1c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb1c-118">-DefaultProfile</span></span>
<span data-ttu-id="bcb1c-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bcb1c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bcb1c-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="bcb1c-120">-FriendlyName</span></span>
<span data-ttu-id="bcb1c-121">Az ASR replikációs házirend rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcb1c-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="bcb1c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bcb1c-122">-Name</span></span>
<span data-ttu-id="bcb1c-123">Az ASR replikációs házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcb1c-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="bcb1c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb1c-124">CommonParameters</span></span>
<span data-ttu-id="bcb1c-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb1c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb1c-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcb1c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb1c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcb1c-127">INPUTS</span></span>

### <span data-ttu-id="bcb1c-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="bcb1c-128">None</span></span>

## <span data-ttu-id="bcb1c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcb1c-129">OUTPUTS</span></span>

### <span data-ttu-id="bcb1c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="bcb1c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="bcb1c-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bcb1c-131">NOTES</span></span>

## <span data-ttu-id="bcb1c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bcb1c-132">RELATED LINKS</span></span>

[<span data-ttu-id="bcb1c-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="bcb1c-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="bcb1c-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="bcb1c-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
