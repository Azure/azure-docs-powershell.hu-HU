---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194072"
---
# <span data-ttu-id="a35a4-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="a35a4-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="a35a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a35a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a35a4-103">A támogatott kiszolgálói változók és a rendelkezésre álló kérések és válaszok fejlécének beszerzése.</span><span class="sxs-lookup"><span data-stu-id="a35a4-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="a35a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a35a4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="a35a4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a35a4-105">DESCRIPTION</span></span>
<span data-ttu-id="a35a4-106">A **Get-AzApplicationGatewayAvailableServerVariableAndHeader** parancsmag a támogatott kiszolgálói változókat és a rendelkezésre álló kérések és válaszok fejlécét kapja.</span><span class="sxs-lookup"><span data-stu-id="a35a4-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="a35a4-107">A változók és a fejlécek listájának beszerzéséhez használható paraméterek.</span><span class="sxs-lookup"><span data-stu-id="a35a4-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="a35a4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a35a4-108">EXAMPLES</span></span>

### <span data-ttu-id="a35a4-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a35a4-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="a35a4-110">Ez a parancs az összes elérhető kiszolgálói változót visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="a35a4-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="a35a4-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="a35a4-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="a35a4-112">Ez a parancs az összes rendelkezésre álló kérés fejlécét visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="a35a4-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="a35a4-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="a35a4-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="a35a4-114">Ez a parancs az összes elérhető válasz fejlécét visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="a35a4-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="a35a4-115">4. példa</span><span class="sxs-lookup"><span data-stu-id="a35a4-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="a35a4-116">Ez a parancs az összes elérhető kiszolgálói változót, kérést és válasz fejlécet visszaadja.</span><span class="sxs-lookup"><span data-stu-id="a35a4-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="a35a4-117">Példa 5</span><span class="sxs-lookup"><span data-stu-id="a35a4-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="a35a4-118">Ez a parancs az összes elérhető kiszolgálói változót, kérést és válasz fejlécet visszaadja.</span><span class="sxs-lookup"><span data-stu-id="a35a4-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="a35a4-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a35a4-119">PARAMETERS</span></span>

### <span data-ttu-id="a35a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a35a4-120">-DefaultProfile</span></span>
<span data-ttu-id="a35a4-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a35a4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a35a4-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="a35a4-122">-RequestHeader</span></span>
<span data-ttu-id="a35a4-123">Az Application Gateway elérhető kérések fejlécei.</span><span class="sxs-lookup"><span data-stu-id="a35a4-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="a35a4-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="a35a4-124">-ResponseHeader</span></span>
<span data-ttu-id="a35a4-125">Az alkalmazás-átjáró elérhető válasz fejléce.</span><span class="sxs-lookup"><span data-stu-id="a35a4-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="a35a4-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="a35a4-126">-ServerVariable</span></span>
<span data-ttu-id="a35a4-127">Az alkalmazás-átjáró elérhető kiszolgálói változói.</span><span class="sxs-lookup"><span data-stu-id="a35a4-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="a35a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a35a4-128">CommonParameters</span></span>
<span data-ttu-id="a35a4-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a35a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a35a4-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a35a4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a35a4-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a35a4-131">INPUTS</span></span>

### <span data-ttu-id="a35a4-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="a35a4-132">None</span></span>

## <span data-ttu-id="a35a4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a35a4-133">OUTPUTS</span></span>

### <span data-ttu-id="a35a4-134">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="a35a4-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="a35a4-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a35a4-135">NOTES</span></span>
<span data-ttu-id="a35a4-136">**Lista – a AzApplicationGatewayAvailableServerVariableAndHeader** a **Get-AzApplicationGatewayAvailableServerVariableAndHeader** parancsmag aliasa.</span><span class="sxs-lookup"><span data-stu-id="a35a4-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="a35a4-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a35a4-137">RELATED LINKS</span></span>