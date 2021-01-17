---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 59d1c7fa5d546652d8976dc42739c2e483164999
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335166"
---
# <span data-ttu-id="c827d-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="c827d-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="c827d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c827d-102">SYNOPSIS</span></span>

<span data-ttu-id="c827d-103">Beveszi az Azure Defender csomagokat egy előfizetéshez az Azure Biztonsági központban.</span><span class="sxs-lookup"><span data-stu-id="c827d-103">Gets the Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="c827d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c827d-104">SYNTAX</span></span>

### <span data-ttu-id="c827d-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c827d-105">SubscriptionScope (Default)</span></span>

```powershell
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c827d-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c827d-106">SubscriptionLevelResource</span></span>

```powershell
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c827d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c827d-107">ResourceId</span></span>

```powershell
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c827d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c827d-108">DESCRIPTION</span></span>

<span data-ttu-id="c827d-109">Ezzel a parancsmagkal előfizetésenként megtekintheti az egyes Azure Defender-csomagokat.</span><span class="sxs-lookup"><span data-stu-id="c827d-109">You can view each Azure Defender plan, per subscription, using this cmdlet.</span></span>

<span data-ttu-id="c827d-110">Az Azure Defenderről és a rendelkezésre álló csomagokról további információt az Azure Defender – [Bevezetés szolgáltatásban talál.](https://docs.microsoft.com/azure/security-center/azure-defender)</span><span class="sxs-lookup"><span data-stu-id="c827d-110">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="c827d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c827d-111">EXAMPLES</span></span>

### <span data-ttu-id="c827d-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="c827d-112">Example 1</span></span>

```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                   Name                      PricingTier    FreeTrialRemainingTime
--                                                                                                                   ----                      -----------    ----------------------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines            VirtualMachines           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/Sqlservers                 SqlServers                Standard       00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices                AppServices               Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts            StorageAccounts           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlserverVirtualMachines   SqlservervirtualMachines  Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService          KubernetesService         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry          ContainerRegistry         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults                  KeyVaults                 Free           00:00:00
```

<span data-ttu-id="c827d-113">Lekérte az előfizetéshez szükséges Azure Defender-előfizetések állapotát.</span><span class="sxs-lookup"><span data-stu-id="c827d-113">Gets the status of each Azure Defender plan for the subscription.</span></span>



### <span data-ttu-id="c827d-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c827d-114">Example 2</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -ResourceId
```

<span data-ttu-id="c827d-115">Az adott erőforrás-azonosító árazási adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c827d-115">Gets pricing details of the specific resource ID.</span></span> <span data-ttu-id="c827d-116">Ahol az ResourceId az egyik visszaadott `Get-AzSecurityPricing` id.</span><span class="sxs-lookup"><span data-stu-id="c827d-116">Where ResourceId is one of the IDs returned by `Get-AzSecurityPricing`.</span></span>

### <span data-ttu-id="c827d-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="c827d-117">Example 3</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -Name
```

<span data-ttu-id="c827d-118">Az Azure Defender nevű csomag árazási adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c827d-118">Gets pricing details of the named Azure Defender plan.</span></span> <span data-ttu-id="c827d-119">Hol `name` van az eredményül adott nevek `Get-AzSecurityPricing` egyike.</span><span class="sxs-lookup"><span data-stu-id="c827d-119">Where `name` is one of the names returned by `Get-AzSecurityPricing`.</span></span>


## <span data-ttu-id="c827d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c827d-120">PARAMETERS</span></span>

### <span data-ttu-id="c827d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c827d-121">-DefaultProfile</span></span>

<span data-ttu-id="c827d-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c827d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c827d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c827d-123">-Name</span></span>

<span data-ttu-id="c827d-124">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c827d-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c827d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c827d-125">-ResourceId</span></span>

<span data-ttu-id="c827d-126">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c827d-126">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c827d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c827d-127">CommonParameters</span></span>

<span data-ttu-id="c827d-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c827d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c827d-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c827d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c827d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c827d-130">INPUTS</span></span>

### <span data-ttu-id="c827d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c827d-131">System.String</span></span>

## <span data-ttu-id="c827d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c827d-132">OUTPUTS</span></span>

### <span data-ttu-id="c827d-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="c827d-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="c827d-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c827d-134">NOTES</span></span>

## <span data-ttu-id="c827d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c827d-135">RELATED LINKS</span></span>
