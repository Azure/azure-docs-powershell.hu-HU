---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 168223e9e442b7aa37da11f3a1e0a092c3cb3efc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841217"
---
# <span data-ttu-id="4e395-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4e395-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="4e395-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e395-102">SYNOPSIS</span></span>
<span data-ttu-id="4e395-103">Eltávolítja a back-end HTTP-beállításokat egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="4e395-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="4e395-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e395-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e395-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e395-105">DESCRIPTION</span></span>
<span data-ttu-id="4e395-106">Az Remove-AzApplicationGatewayBackendHttpSetting parancsmag eltávolítja a HTTP-beállításokat az Azure Application Gateway-ből.</span><span class="sxs-lookup"><span data-stu-id="4e395-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="4e395-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4e395-107">EXAMPLES</span></span>

### <span data-ttu-id="4e395-108">Példa 1: a back-end HTTP-beállítások eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="4e395-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="4e395-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4e395-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="4e395-110">A második parancs eltávolítja a BackEndSetting02 nevű back-end HTTP-beállítást az $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="4e395-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4e395-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e395-111">PARAMETERS</span></span>

### <span data-ttu-id="4e395-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e395-112">-ApplicationGateway</span></span>
<span data-ttu-id="4e395-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből a parancsmag eltávolítja a back-end HTTP-beállításokat.</span><span class="sxs-lookup"><span data-stu-id="4e395-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e395-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e395-114">-DefaultProfile</span></span>
<span data-ttu-id="4e395-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e395-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e395-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e395-116">-Name</span></span>
<span data-ttu-id="4e395-117">A parancsmag által eltávolított back-end HTTP-beállítások nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e395-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e395-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e395-118">CommonParameters</span></span>
<span data-ttu-id="4e395-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e395-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e395-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e395-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e395-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e395-121">INPUTS</span></span>

### <span data-ttu-id="4e395-122">System. String</span><span class="sxs-lookup"><span data-stu-id="4e395-122">System.String</span></span>

## <span data-ttu-id="4e395-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e395-123">OUTPUTS</span></span>

### <span data-ttu-id="4e395-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e395-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4e395-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e395-125">NOTES</span></span>

## <span data-ttu-id="4e395-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e395-126">RELATED LINKS</span></span>

[<span data-ttu-id="4e395-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4e395-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="4e395-128">Új – AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4e395-128">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="4e395-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4e395-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="4e395-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4e395-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>]()

