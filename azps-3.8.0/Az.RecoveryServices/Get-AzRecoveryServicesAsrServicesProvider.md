---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 4be24acddf1f02ecd9216a06690958feed2d6c57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010608"
---
# <span data-ttu-id="71f62-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="71f62-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="71f62-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71f62-102">SYNOPSIS</span></span>
<span data-ttu-id="71f62-103">A helyreállítási szolgáltatások boltozatához regisztrált ASR-helyreállítási szolgáltató adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="71f62-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="71f62-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71f62-104">SYNTAX</span></span>

### <span data-ttu-id="71f62-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71f62-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71f62-106">ByName</span><span class="sxs-lookup"><span data-stu-id="71f62-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71f62-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="71f62-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71f62-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="71f62-108">DESCRIPTION</span></span>
<span data-ttu-id="71f62-109">A **Get-AzRecoveryServicesAsrServicesProvider** parancsmag információt kap az Azure webhely-helyreállítási szolgáltatónál a boltozatban.</span><span class="sxs-lookup"><span data-stu-id="71f62-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="71f62-110">Példák</span><span class="sxs-lookup"><span data-stu-id="71f62-110">EXAMPLES</span></span>

### <span data-ttu-id="71f62-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="71f62-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="71f62-112">Felsorolja az összes ASR-replikációs szolgáltatót, amely a megadott anyagnak megfelelő helyreállítási szolgáltatások boltozatához van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="71f62-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="71f62-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71f62-113">PARAMETERS</span></span>

### <span data-ttu-id="71f62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71f62-114">-DefaultProfile</span></span>
<span data-ttu-id="71f62-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71f62-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="71f62-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="71f62-116">-Fabric</span></span>
<span data-ttu-id="71f62-117">Az ASR-szerkezet objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="71f62-117">Specifies the ASR fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71f62-118">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="71f62-118">-FriendlyName</span></span>
<span data-ttu-id="71f62-119">Az ASR-helyreállítási szolgáltató rövid nevét adja meg, amelyből részletesen tájékozódhat.</span><span class="sxs-lookup"><span data-stu-id="71f62-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="71f62-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="71f62-120">-Name</span></span>
<span data-ttu-id="71f62-121">Annak az ASR-helyreállítási szolgáltatónak a nevét adja meg, amelyről részleteket szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="71f62-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="71f62-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f62-122">CommonParameters</span></span>
<span data-ttu-id="71f62-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71f62-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f62-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="71f62-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f62-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71f62-125">INPUTS</span></span>

### <span data-ttu-id="71f62-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="71f62-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="71f62-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71f62-127">OUTPUTS</span></span>

### <span data-ttu-id="71f62-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="71f62-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="71f62-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71f62-129">NOTES</span></span>

## <span data-ttu-id="71f62-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71f62-130">RELATED LINKS</span></span>

[<span data-ttu-id="71f62-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="71f62-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="71f62-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="71f62-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
