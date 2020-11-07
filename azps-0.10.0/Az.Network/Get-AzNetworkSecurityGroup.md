---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: beb2b723a0b72f7ab485846f6f55fabd4e6ef9aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841601"
---
# <span data-ttu-id="5be14-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5be14-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="5be14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5be14-102">SYNOPSIS</span></span>
<span data-ttu-id="5be14-103">Hálózati biztonsági csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="5be14-103">Gets a network security group.</span></span>

## <span data-ttu-id="5be14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5be14-104">SYNTAX</span></span>

### <span data-ttu-id="5be14-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="5be14-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5be14-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="5be14-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5be14-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5be14-107">DESCRIPTION</span></span>
<span data-ttu-id="5be14-108">A **Get-AzNetworkSecurityGroup** parancsmag Azure hálózati biztonsági csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="5be14-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="5be14-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5be14-109">EXAMPLES</span></span>

### <span data-ttu-id="5be14-110">1: meglévő hálózati biztonsági csoport beolvasása</span><span class="sxs-lookup"><span data-stu-id="5be14-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="5be14-111">Ez a parancs a "nsg1" erőforráscsoport "rg1" erőforráscsoporthoz tartozó Azure Network biztonsági csoportjának tartalmát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="5be14-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="5be14-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5be14-112">PARAMETERS</span></span>

### <span data-ttu-id="5be14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5be14-113">-DefaultProfile</span></span>
<span data-ttu-id="5be14-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5be14-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5be14-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="5be14-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5be14-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5be14-116">-Name</span></span>
<span data-ttu-id="5be14-117">Annak a hálózati biztonsági csoportnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="5be14-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5be14-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5be14-118">-ResourceGroupName</span></span>
<span data-ttu-id="5be14-119">Annak az erőforráscsoport-csoportnak a neve, amelyhez a hálózat biztonsági csoportja tartozik.</span><span class="sxs-lookup"><span data-stu-id="5be14-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5be14-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5be14-120">CommonParameters</span></span>
<span data-ttu-id="5be14-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5be14-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5be14-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5be14-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5be14-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5be14-123">INPUTS</span></span>

## <span data-ttu-id="5be14-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5be14-124">OUTPUTS</span></span>

### <span data-ttu-id="5be14-125">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5be14-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="5be14-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5be14-126">NOTES</span></span>

## <span data-ttu-id="5be14-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5be14-127">RELATED LINKS</span></span>

[<span data-ttu-id="5be14-128">Új – AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5be14-128">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="5be14-129">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5be14-129">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="5be14-130">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5be14-130">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


