---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
ms.openlocfilehash: 374f23ad90b5ff0b9c48b33285b80cf44265ed0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502028"
---
# <span data-ttu-id="457ac-101">Get-AzureRmApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="457ac-101">Get-AzureRmApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="457ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="457ac-102">SYNOPSIS</span></span>
<span data-ttu-id="457ac-103">Az Application Gateway backend-állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="457ac-103">Gets application gateway backend health.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="457ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="457ac-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String>
 [-ExpandResource <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="457ac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="457ac-105">DESCRIPTION</span></span>
<span data-ttu-id="457ac-106">A Get-AzureRmApplicationGatewayBackendHealth parancsmag az Application Gateway backend állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="457ac-106">The Get-AzureRmApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="457ac-107">Példák</span><span class="sxs-lookup"><span data-stu-id="457ac-107">EXAMPLES</span></span>

### <span data-ttu-id="457ac-108">Példa 1: kibontott erőforrások nélkül kapja meg a backend állapotát.</span><span class="sxs-lookup"><span data-stu-id="457ac-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="457ac-109">Ez a parancs megkapja a ApplicationGateway01 nevű, az ResourceGroup01 nevű erőforráscsoporthoz tartozó, az nevű erőforráscsoport állapotát, és a $BackendHealth változóban tárolja az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="457ac-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="457ac-110">Példa 1: a backend-állapot beolvasása a kibontott erőforrásokkal.</span><span class="sxs-lookup"><span data-stu-id="457ac-110">Example 1: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="457ac-111">Ez a parancs a ApplicationGateway01 nevű ResourceGroup01 nevű erőforráscsoporthoz tartozó, az nevű erőforráscsoporthoz tartozó, és a $BackendHealth változóban tárolja a backend (bővített erőforrások) állapotát.</span><span class="sxs-lookup"><span data-stu-id="457ac-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="457ac-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="457ac-112">PARAMETERS</span></span>

### <span data-ttu-id="457ac-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="457ac-113">-AsJob</span></span>
<span data-ttu-id="457ac-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="457ac-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="457ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="457ac-115">-DefaultProfile</span></span>
<span data-ttu-id="457ac-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="457ac-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="457ac-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="457ac-117">-ExpandResource</span></span>
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

### <span data-ttu-id="457ac-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="457ac-118">-Name</span></span>
<span data-ttu-id="457ac-119">Annak az alkalmazás-átjárónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="457ac-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="457ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="457ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="457ac-121">Az alkalmazás-átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="457ac-121">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="457ac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="457ac-122">CommonParameters</span></span>
<span data-ttu-id="457ac-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="457ac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="457ac-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="457ac-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="457ac-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="457ac-125">INPUTS</span></span>

### <span data-ttu-id="457ac-126">System. String</span><span class="sxs-lookup"><span data-stu-id="457ac-126">System.String</span></span>

## <span data-ttu-id="457ac-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="457ac-127">OUTPUTS</span></span>

### <span data-ttu-id="457ac-128">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="457ac-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="457ac-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="457ac-129">NOTES</span></span>
<span data-ttu-id="457ac-130">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="457ac-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="457ac-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="457ac-131">RELATED LINKS</span></span>

[<span data-ttu-id="457ac-132">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="457ac-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)
