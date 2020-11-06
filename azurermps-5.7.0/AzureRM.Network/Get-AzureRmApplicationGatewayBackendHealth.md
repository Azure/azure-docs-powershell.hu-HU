---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
ms.openlocfilehash: 6e6a2bef9ea6bc237db97139bcc7e9e7a0624fd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493115"
---
# <span data-ttu-id="f8ffb-101">Get-AzureRmApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="f8ffb-101">Get-AzureRmApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="f8ffb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ffb-103">Az Application Gateway backend-állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="f8ffb-103">Gets application gateway backend health.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8ffb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8ffb-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String>
 [-ExpandResource <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8ffb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8ffb-105">DESCRIPTION</span></span>
<span data-ttu-id="f8ffb-106">A Get-AzureRmApplicationGatewayBackendHealth parancsmag az Application Gateway backend állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="f8ffb-106">The Get-AzureRmApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="f8ffb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f8ffb-107">EXAMPLES</span></span>

### <span data-ttu-id="f8ffb-108">--------------------------Példa 1: kibontott erőforrások nélkül kapja meg a backend állapotát.</span><span class="sxs-lookup"><span data-stu-id="f8ffb-108">--------------------------  Example 1: Gets backend health without expanded resources.</span></span>  --------------------------
```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="f8ffb-109">Ez a parancs megkapja a ApplicationGateway01 nevű, az ResourceGroup01 nevű erőforráscsoporthoz tartozó, az nevű erőforráscsoport állapotát, és a $BackendHealth változóban tárolja az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="f8ffb-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="f8ffb-110">--------------------------Példa 1: kibontott erőforrásokkal kapja meg a backend állapotát.</span><span class="sxs-lookup"><span data-stu-id="f8ffb-110">--------------------------  Example 1: Gets backend health with expanded resources.</span></span>  --------------------------
```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="f8ffb-111">Ez a parancs a ApplicationGateway01 nevű ResourceGroup01 nevű erőforráscsoporthoz tartozó, az nevű erőforráscsoporthoz tartozó, és a $BackendHealth változóban tárolja a backend (bővített erőforrások) állapotát.</span><span class="sxs-lookup"><span data-stu-id="f8ffb-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="f8ffb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8ffb-112">PARAMETERS</span></span>

### <span data-ttu-id="f8ffb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8ffb-113">-AsJob</span></span>
<span data-ttu-id="f8ffb-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f8ffb-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ffb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ffb-115">-DefaultProfile</span></span>
<span data-ttu-id="f8ffb-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8ffb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8ffb-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f8ffb-117">-ExpandResource</span></span>
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

### <span data-ttu-id="f8ffb-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f8ffb-118">-Name</span></span>
<span data-ttu-id="f8ffb-119">Annak az alkalmazás-átjárónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="f8ffb-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ffb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8ffb-120">-ResourceGroupName</span></span>
<span data-ttu-id="f8ffb-121">Az alkalmazás-átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8ffb-121">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ffb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ffb-122">CommonParameters</span></span>
<span data-ttu-id="f8ffb-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8ffb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ffb-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8ffb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ffb-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8ffb-125">INPUTS</span></span>

### <span data-ttu-id="f8ffb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f8ffb-126">System.String</span></span>

## <span data-ttu-id="f8ffb-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8ffb-127">OUTPUTS</span></span>

### <span data-ttu-id="f8ffb-128">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="f8ffb-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="f8ffb-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8ffb-129">NOTES</span></span>
<span data-ttu-id="f8ffb-130">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="f8ffb-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f8ffb-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8ffb-131">RELATED LINKS</span></span>

[<span data-ttu-id="f8ffb-132">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f8ffb-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

