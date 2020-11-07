---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: e0a9bd49ca49ae4df1ae83d9c93a191f406c442a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848165"
---
# <span data-ttu-id="a383d-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a383d-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="a383d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a383d-102">SYNOPSIS</span></span>
<span data-ttu-id="a383d-103">Hálózati biztonsági csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="a383d-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a383d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a383d-104">SYNTAX</span></span>

### <span data-ttu-id="a383d-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="a383d-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a383d-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="a383d-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a383d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a383d-107">DESCRIPTION</span></span>
<span data-ttu-id="a383d-108">A **Get-AzureRmNetworkSecurityGroup** parancsmag Azure hálózati biztonsági csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="a383d-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="a383d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a383d-109">EXAMPLES</span></span>

### <span data-ttu-id="a383d-110">1: meglévő hálózati biztonsági csoport beolvasása</span><span class="sxs-lookup"><span data-stu-id="a383d-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="a383d-111">Ez a parancs a "nsg1" erőforráscsoport "rg1" erőforráscsoporthoz tartozó Azure Network biztonsági csoportjának tartalmát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="a383d-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="a383d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a383d-112">PARAMETERS</span></span>

### <span data-ttu-id="a383d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a383d-113">-DefaultProfile</span></span>
<span data-ttu-id="a383d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a383d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a383d-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="a383d-115">-ExpandResource</span></span>
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

### <span data-ttu-id="a383d-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a383d-116">-Name</span></span>
<span data-ttu-id="a383d-117">Annak a hálózati biztonsági csoportnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="a383d-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a383d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a383d-118">-ResourceGroupName</span></span>
<span data-ttu-id="a383d-119">Annak az erőforráscsoport-csoportnak a neve, amelyhez a hálózat biztonsági csoportja tartozik.</span><span class="sxs-lookup"><span data-stu-id="a383d-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

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

### <span data-ttu-id="a383d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a383d-120">CommonParameters</span></span>
<span data-ttu-id="a383d-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a383d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a383d-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a383d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a383d-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a383d-123">INPUTS</span></span>

## <span data-ttu-id="a383d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a383d-124">OUTPUTS</span></span>

### <span data-ttu-id="a383d-125">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a383d-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a383d-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a383d-126">NOTES</span></span>

## <span data-ttu-id="a383d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a383d-127">RELATED LINKS</span></span>

[<span data-ttu-id="a383d-128">Új – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a383d-128">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="a383d-129">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a383d-129">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="a383d-130">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a383d-130">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


