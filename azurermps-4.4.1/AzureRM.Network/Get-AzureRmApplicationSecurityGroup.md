---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 704c4c2a11cc83136481573190e745d7a4b2c83f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504867"
---
# <span data-ttu-id="05eb9-101">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="05eb9-101">Get-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="05eb9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="05eb9-103">Bekapja az alkalmazás biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="05eb9-103">Gets an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05eb9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05eb9-104">SYNTAX</span></span>

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05eb9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="05eb9-105">DESCRIPTION</span></span>
<span data-ttu-id="05eb9-106">A **Get-AzureRmApplicationSecurityGroup** parancsmag az alkalmazások biztonsági csoportját kapja.</span><span class="sxs-lookup"><span data-stu-id="05eb9-106">The **Get-AzureRmApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="05eb9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="05eb9-107">EXAMPLES</span></span>

### <span data-ttu-id="05eb9-108">Példa 1: az összes alkalmazás biztonsági csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="05eb9-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

<span data-ttu-id="05eb9-109">A fenti parancs a minden alkalmazás biztonsági csoportját visszaállítja az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="05eb9-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="05eb9-110">2. példa: az alkalmazás biztonsági csoportjainak beolvasása egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="05eb9-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="05eb9-111">A fenti parancs az erőforráscsoport MyResourceGroup tartozó összes alkalmazás biztonsági csoportját visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="05eb9-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="05eb9-112">3. példa: egy adott alkalmazás biztonsági csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="05eb9-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="05eb9-113">A fenti parancs az MyApplicationSecurityGroup MyResourceGroup az alkalmazás biztonsági csoportjának értékét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="05eb9-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="05eb9-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05eb9-114">PARAMETERS</span></span>

### <span data-ttu-id="05eb9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05eb9-115">-DefaultProfile</span></span>
<span data-ttu-id="05eb9-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05eb9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05eb9-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="05eb9-117">-Name</span></span>
<span data-ttu-id="05eb9-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="05eb9-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05eb9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05eb9-119">-ResourceGroupName</span></span>
<span data-ttu-id="05eb9-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="05eb9-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05eb9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05eb9-121">CommonParameters</span></span>
<span data-ttu-id="05eb9-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05eb9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05eb9-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05eb9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05eb9-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05eb9-124">INPUTS</span></span>

### <span data-ttu-id="05eb9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="05eb9-125">System.String</span></span>

## <span data-ttu-id="05eb9-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05eb9-126">OUTPUTS</span></span>

### <span data-ttu-id="05eb9-127">Microsoft. Azure. commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="05eb9-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="05eb9-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05eb9-128">NOTES</span></span>

## <span data-ttu-id="05eb9-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05eb9-129">RELATED LINKS</span></span>

[<span data-ttu-id="05eb9-130">Új – AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="05eb9-130">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="05eb9-131">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="05eb9-131">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="05eb9-132">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05eb9-132">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="05eb9-133">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="05eb9-133">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)