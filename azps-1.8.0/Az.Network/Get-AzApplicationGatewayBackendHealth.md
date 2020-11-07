---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: eb4415f4c61fd97543bd0e50de6a0a3737f435f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670664"
---
# <span data-ttu-id="daef1-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="daef1-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="daef1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="daef1-102">SYNOPSIS</span></span>
<span data-ttu-id="daef1-103">Az Application Gateway backend-állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="daef1-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="daef1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="daef1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daef1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="daef1-105">DESCRIPTION</span></span>
<span data-ttu-id="daef1-106">A Get-AzApplicationGatewayBackendHealth parancsmag az Application Gateway backend állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="daef1-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="daef1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="daef1-107">EXAMPLES</span></span>

### <span data-ttu-id="daef1-108">Példa 1: kibontott erőforrások nélkül kapja meg a backend állapotát.</span><span class="sxs-lookup"><span data-stu-id="daef1-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="daef1-109">Ez a parancs megkapja a ApplicationGateway01 nevű, az ResourceGroup01 nevű erőforráscsoporthoz tartozó, az nevű erőforráscsoport állapotát, és a $BackendHealth változóban tárolja az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="daef1-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="daef1-110">2. példa: a backend állapotát kibontott erőforrásokkal kapja.</span><span class="sxs-lookup"><span data-stu-id="daef1-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="daef1-111">Ez a parancs a ApplicationGateway01 nevű ResourceGroup01 nevű erőforráscsoporthoz tartozó, az nevű erőforráscsoporthoz tartozó, és a $BackendHealth változóban tárolja a backend (bővített erőforrások) állapotát.</span><span class="sxs-lookup"><span data-stu-id="daef1-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="daef1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="daef1-112">PARAMETERS</span></span>

### <span data-ttu-id="daef1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="daef1-113">-AsJob</span></span>
<span data-ttu-id="daef1-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="daef1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="daef1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daef1-115">-DefaultProfile</span></span>
<span data-ttu-id="daef1-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="daef1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daef1-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="daef1-117">-ExpandResource</span></span>
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

### <span data-ttu-id="daef1-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="daef1-118">-Name</span></span>
<span data-ttu-id="daef1-119">Annak az alkalmazás-átjárónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="daef1-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="daef1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daef1-120">-ResourceGroupName</span></span>
<span data-ttu-id="daef1-121">Az alkalmazás-átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="daef1-121">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="daef1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daef1-122">CommonParameters</span></span>
<span data-ttu-id="daef1-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="daef1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daef1-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="daef1-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daef1-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="daef1-125">INPUTS</span></span>

### <span data-ttu-id="daef1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="daef1-126">System.String</span></span>

## <span data-ttu-id="daef1-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="daef1-127">OUTPUTS</span></span>

### <span data-ttu-id="daef1-128">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="daef1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="daef1-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="daef1-129">NOTES</span></span>
<span data-ttu-id="daef1-130">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="daef1-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="daef1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="daef1-131">RELATED LINKS</span></span>

[<span data-ttu-id="daef1-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daef1-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

