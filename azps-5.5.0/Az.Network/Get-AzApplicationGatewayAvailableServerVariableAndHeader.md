---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157130"
---
# <span data-ttu-id="c0422-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="c0422-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="c0422-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0422-102">SYNOPSIS</span></span>
<span data-ttu-id="c0422-103">Szerezze be a támogatott kiszolgálói változókat, valamint az elérhető kérés- és válaszfejléceket.</span><span class="sxs-lookup"><span data-stu-id="c0422-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="c0422-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c0422-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="c0422-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c0422-105">DESCRIPTION</span></span>
<span data-ttu-id="c0422-106">A **Get-AzApplicationGatewayAvailableServerVariableAndHeader** parancsmag megkapja a támogatott kiszolgálói változókat, valamint a rendelkezésre álló kérés- és válaszfejléceket.</span><span class="sxs-lookup"><span data-stu-id="c0422-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="c0422-107">Paramétereket használva lekértheti a változókat és a fejléclistákat.</span><span class="sxs-lookup"><span data-stu-id="c0422-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="c0422-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c0422-108">EXAMPLES</span></span>

### <span data-ttu-id="c0422-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="c0422-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="c0422-110">Ez a parancs az összes rendelkezésre álló kiszolgálói változót visszaadja.</span><span class="sxs-lookup"><span data-stu-id="c0422-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="c0422-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="c0422-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="c0422-112">Ez a parancs az összes elérhető kérelemfejlécet visszaadja.</span><span class="sxs-lookup"><span data-stu-id="c0422-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="c0422-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="c0422-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="c0422-114">Ez a parancs az összes elérhető válaszfejlécet visszaadja.</span><span class="sxs-lookup"><span data-stu-id="c0422-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="c0422-115">4. példa</span><span class="sxs-lookup"><span data-stu-id="c0422-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="c0422-116">Ez a parancs az összes rendelkezésre álló kiszolgálói változót, kérés- és válaszfejlécet visszaadja.</span><span class="sxs-lookup"><span data-stu-id="c0422-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="c0422-117">5. példa</span><span class="sxs-lookup"><span data-stu-id="c0422-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="c0422-118">Ez a parancs az összes elérhető kiszolgálóváltozót, kérés- és válaszfejlécet visszaadja.</span><span class="sxs-lookup"><span data-stu-id="c0422-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="c0422-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0422-119">PARAMETERS</span></span>

### <span data-ttu-id="c0422-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0422-120">-DefaultProfile</span></span>
<span data-ttu-id="c0422-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0422-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0422-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="c0422-122">-RequestHeader</span></span>
<span data-ttu-id="c0422-123">Az alkalmazás átjárója elérhető kérésfejlécek.</span><span class="sxs-lookup"><span data-stu-id="c0422-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="c0422-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="c0422-124">-ResponseHeader</span></span>
<span data-ttu-id="c0422-125">Az Alkalmazás átjáró elérhető válaszfejlécei.</span><span class="sxs-lookup"><span data-stu-id="c0422-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="c0422-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="c0422-126">-ServerVariable</span></span>
<span data-ttu-id="c0422-127">Az alkalmazás átjárója elérhető kiszolgálóváltozók.</span><span class="sxs-lookup"><span data-stu-id="c0422-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="c0422-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0422-128">CommonParameters</span></span>
<span data-ttu-id="c0422-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0422-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0422-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0422-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0422-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0422-131">INPUTS</span></span>

### <span data-ttu-id="c0422-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="c0422-132">None</span></span>

## <span data-ttu-id="c0422-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0422-133">OUTPUTS</span></span>

### <span data-ttu-id="c0422-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="c0422-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="c0422-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c0422-135">NOTES</span></span>
<span data-ttu-id="c0422-136">**A List-AzApplicationGatewayAvailableServerVariableAndHeader** a **Get-AzApplicationGatewayAvailableServerVariableAndHeader** parancsmag aliasa.</span><span class="sxs-lookup"><span data-stu-id="c0422-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="c0422-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0422-137">RELATED LINKS</span></span>
