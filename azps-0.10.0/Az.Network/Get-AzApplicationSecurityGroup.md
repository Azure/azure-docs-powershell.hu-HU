---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: b23901a79262f4eb63e34b99c10b82442cb2fe6a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841685"
---
# <span data-ttu-id="4fb94-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4fb94-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="4fb94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fb94-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb94-103">Bekapja az alkalmazás biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="4fb94-103">Gets an application security group.</span></span>

## <span data-ttu-id="4fb94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fb94-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fb94-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fb94-105">DESCRIPTION</span></span>
<span data-ttu-id="4fb94-106">A **Get-AzApplicationSecurityGroup** parancsmag az alkalmazások biztonsági csoportját kapja.</span><span class="sxs-lookup"><span data-stu-id="4fb94-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="4fb94-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4fb94-107">EXAMPLES</span></span>

### <span data-ttu-id="4fb94-108">Példa 1: az összes alkalmazás biztonsági csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="4fb94-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup
```

<span data-ttu-id="4fb94-109">A fenti parancs a minden alkalmazás biztonsági csoportját visszaállítja az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="4fb94-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="4fb94-110">2. példa: az alkalmazás biztonsági csoportjainak beolvasása egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="4fb94-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="4fb94-111">A fenti parancs az erőforráscsoport MyResourceGroup tartozó összes alkalmazás biztonsági csoportját visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="4fb94-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="4fb94-112">3. példa: egy adott alkalmazás biztonsági csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="4fb94-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="4fb94-113">A fenti parancs az MyApplicationSecurityGroup MyResourceGroup az alkalmazás biztonsági csoportjának értékét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="4fb94-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="4fb94-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fb94-114">PARAMETERS</span></span>

### <span data-ttu-id="4fb94-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb94-115">-DefaultProfile</span></span>
<span data-ttu-id="4fb94-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fb94-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fb94-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4fb94-117">-Name</span></span>
<span data-ttu-id="4fb94-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4fb94-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb94-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb94-119">-ResourceGroupName</span></span>
<span data-ttu-id="4fb94-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4fb94-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb94-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb94-121">CommonParameters</span></span>
<span data-ttu-id="4fb94-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fb94-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb94-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb94-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb94-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fb94-124">INPUTS</span></span>

### <span data-ttu-id="4fb94-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4fb94-125">System.String</span></span>

## <span data-ttu-id="4fb94-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fb94-126">OUTPUTS</span></span>

### <span data-ttu-id="4fb94-127">Microsoft. Azure. commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4fb94-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="4fb94-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fb94-128">NOTES</span></span>

## <span data-ttu-id="4fb94-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fb94-129">RELATED LINKS</span></span>

[<span data-ttu-id="4fb94-130">Új – AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4fb94-130">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="4fb94-131">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4fb94-131">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="4fb94-132">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4fb94-132">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4fb94-133">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4fb94-133">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
