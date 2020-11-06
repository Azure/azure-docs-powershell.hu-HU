---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: dc9934aaee7706e3577039bdb77c5a6a54c29c34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500531"
---
# <span data-ttu-id="db3d5-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db3d5-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="db3d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db3d5-102">SYNOPSIS</span></span>
<span data-ttu-id="db3d5-103">Hálózati biztonsági csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="db3d5-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db3d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db3d5-104">SYNTAX</span></span>

### <span data-ttu-id="db3d5-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="db3d5-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db3d5-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="db3d5-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db3d5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="db3d5-107">DESCRIPTION</span></span>
<span data-ttu-id="db3d5-108">A **Get-AzureRmNetworkSecurityGroup** parancsmag Azure hálózati biztonsági csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="db3d5-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="db3d5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="db3d5-109">EXAMPLES</span></span>

### <span data-ttu-id="db3d5-110">1: meglévő hálózati biztonsági csoport beolvasása</span><span class="sxs-lookup"><span data-stu-id="db3d5-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="db3d5-111">Ez a parancs a "nsg1" erőforráscsoport "rg1" erőforráscsoporthoz tartozó Azure Network biztonsági csoportjának tartalmát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="db3d5-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="db3d5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db3d5-112">PARAMETERS</span></span>

### <span data-ttu-id="db3d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db3d5-113">-DefaultProfile</span></span>
<span data-ttu-id="db3d5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db3d5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db3d5-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="db3d5-115">-ExpandResource</span></span>
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

### <span data-ttu-id="db3d5-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db3d5-116">-Name</span></span>
<span data-ttu-id="db3d5-117">Annak a hálózati biztonsági csoportnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="db3d5-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

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

### <span data-ttu-id="db3d5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db3d5-118">-ResourceGroupName</span></span>
<span data-ttu-id="db3d5-119">Annak az erőforráscsoport-csoportnak a neve, amelyhez a hálózat biztonsági csoportja tartozik.</span><span class="sxs-lookup"><span data-stu-id="db3d5-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

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

### <span data-ttu-id="db3d5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db3d5-120">CommonParameters</span></span>
<span data-ttu-id="db3d5-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db3d5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db3d5-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db3d5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db3d5-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db3d5-123">INPUTS</span></span>

### <span data-ttu-id="db3d5-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="db3d5-124">None</span></span>
<span data-ttu-id="db3d5-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="db3d5-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db3d5-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db3d5-126">OUTPUTS</span></span>

### <span data-ttu-id="db3d5-127">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db3d5-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="db3d5-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db3d5-128">NOTES</span></span>

## <span data-ttu-id="db3d5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db3d5-129">RELATED LINKS</span></span>

[<span data-ttu-id="db3d5-130">Új – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db3d5-130">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="db3d5-131">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db3d5-131">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="db3d5-132">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db3d5-132">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


