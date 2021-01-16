---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: 378c6ee91c438bfa70ab8e89e069ad81d3515e33
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354066"
---
# <span data-ttu-id="80d6a-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="80d6a-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="80d6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="80d6a-103">Alkalmazás-átjáró háttér-állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80d6a-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="80d6a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="80d6a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80d6a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="80d6a-105">DESCRIPTION</span></span>
<span data-ttu-id="80d6a-106">A Get-AzApplicationGatewayBackendHealth parancsmag az alkalmazás-átjáró háttér-állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80d6a-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="80d6a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="80d6a-107">EXAMPLES</span></span>

### <span data-ttu-id="80d6a-108">1. példa: Háttér-állapot kibontott erőforrások nélkül.</span><span class="sxs-lookup"><span data-stu-id="80d6a-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="80d6a-109">Ez a parancs az ApplicationGateway01 nevű alkalmazás-átjáró háttér-állapotát kapja meg, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $BackendHealth tárolja.</span><span class="sxs-lookup"><span data-stu-id="80d6a-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="80d6a-110">2. példa: Háttér-állapot kibontott erőforrásokkal.</span><span class="sxs-lookup"><span data-stu-id="80d6a-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="80d6a-111">Ez a parancs az ApplicationGateway01 nevű alkalmazás-átjáró háttér-állapotát kapja vissza (kibontott erőforrásokkal), amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $BackendHealth tárolja.</span><span class="sxs-lookup"><span data-stu-id="80d6a-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="80d6a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80d6a-112">PARAMETERS</span></span>

### <span data-ttu-id="80d6a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80d6a-113">-AsJob</span></span>
<span data-ttu-id="80d6a-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="80d6a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80d6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d6a-115">-DefaultProfile</span></span>
<span data-ttu-id="80d6a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80d6a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80d6a-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="80d6a-117">-ExpandResource</span></span>
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

### <span data-ttu-id="80d6a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="80d6a-118">-Name</span></span>
<span data-ttu-id="80d6a-119">Annak az alkalmazás-átjárónak a nevét adja meg, amelybe a parancsmagot beállítja.</span><span class="sxs-lookup"><span data-stu-id="80d6a-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="80d6a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80d6a-120">-ResourceGroupName</span></span>
<span data-ttu-id="80d6a-121">Az alkalmazás-átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80d6a-121">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="80d6a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d6a-122">CommonParameters</span></span>
<span data-ttu-id="80d6a-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80d6a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d6a-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80d6a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d6a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80d6a-125">INPUTS</span></span>

### <span data-ttu-id="80d6a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="80d6a-126">System.String</span></span>

## <span data-ttu-id="80d6a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80d6a-127">OUTPUTS</span></span>

### <span data-ttu-id="80d6a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="80d6a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="80d6a-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="80d6a-129">NOTES</span></span>
<span data-ttu-id="80d6a-130">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="80d6a-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="80d6a-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80d6a-131">RELATED LINKS</span></span>

[<span data-ttu-id="80d6a-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80d6a-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

