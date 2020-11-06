---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: bd4280f87d397afdcab3f77e8305a0c1ff4b0ed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494414"
---
# <span data-ttu-id="ab046-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ab046-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="ab046-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab046-102">SYNOPSIS</span></span>
<span data-ttu-id="ab046-103">ASR-replikációs házirendek jelentkeznek.</span><span class="sxs-lookup"><span data-stu-id="ab046-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab046-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab046-104">SYNTAX</span></span>

### <span data-ttu-id="ab046-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab046-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab046-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ab046-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab046-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ab046-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab046-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab046-108">DESCRIPTION</span></span>
<span data-ttu-id="ab046-109">A **Get-AzureRmRecoveryServicesAsrPolicy** parancsmag a konfigurált Azure-webhelyek helyreállítási replikációs házirendjeinek vagy egy adott replikációs házirendnek a neve alapján kapja meg a listát.</span><span class="sxs-lookup"><span data-stu-id="ab046-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="ab046-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ab046-110">EXAMPLES</span></span>

### <span data-ttu-id="ab046-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ab046-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy
```

<span data-ttu-id="ab046-112">Retuns a replikációs házirendek listájával</span><span class="sxs-lookup"><span data-stu-id="ab046-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="ab046-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ab046-113">Example 2</span></span>
```
PS C:\>  Get-AzureRmRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="ab046-114">A Retuns replikációs házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="ab046-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="ab046-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="ab046-115">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="ab046-116">A megadott felhasználóbarát névvel rendelkező replikációs házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ab046-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="ab046-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab046-117">PARAMETERS</span></span>

### <span data-ttu-id="ab046-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab046-118">-DefaultProfile</span></span>
<span data-ttu-id="ab046-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab046-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="ab046-120">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="ab046-120">-FriendlyName</span></span>
<span data-ttu-id="ab046-121">Az ASR-replikációs házirend rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab046-121">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab046-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab046-122">-Name</span></span>
<span data-ttu-id="ab046-123">Az ASR-replikációs házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab046-123">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab046-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab046-124">CommonParameters</span></span>
<span data-ttu-id="ab046-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab046-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab046-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab046-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab046-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab046-127">INPUTS</span></span>

### <span data-ttu-id="ab046-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="ab046-128">None</span></span>

## <span data-ttu-id="ab046-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab046-129">OUTPUTS</span></span>

### <span data-ttu-id="ab046-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRPolicy, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ab046-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ab046-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab046-131">NOTES</span></span>

## <span data-ttu-id="ab046-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab046-132">RELATED LINKS</span></span>

[<span data-ttu-id="ab046-133">Új – AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ab046-133">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="ab046-134">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ab046-134">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
