---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365439"
---
# <span data-ttu-id="c71ba-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c71ba-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="c71ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c71ba-102">SYNOPSIS</span></span>
<span data-ttu-id="c71ba-103">A meglévő átjáró kulcsait kapja meg</span><span class="sxs-lookup"><span data-stu-id="c71ba-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="c71ba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c71ba-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c71ba-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c71ba-105">DESCRIPTION</span></span>
<span data-ttu-id="c71ba-106">A **Get-AzApiManagementGatewayKey** parancsmag a meglévő átjáró kulcsait kapja meg</span><span class="sxs-lookup"><span data-stu-id="c71ba-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="c71ba-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c71ba-107">EXAMPLES</span></span>

### <span data-ttu-id="c71ba-108">2. példa: Átjáró létrehozása azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="c71ba-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="c71ba-109">Ez a parancs egy "0123456789" átjáró kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c71ba-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="c71ba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c71ba-110">PARAMETERS</span></span>

### <span data-ttu-id="c71ba-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c71ba-111">-Context</span></span>
<span data-ttu-id="c71ba-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="c71ba-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c71ba-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="c71ba-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c71ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c71ba-114">-DefaultProfile</span></span>
<span data-ttu-id="c71ba-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c71ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c71ba-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="c71ba-116">-GatewayId</span></span>
<span data-ttu-id="c71ba-117">Átjáró azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c71ba-117">Gateway identifier.</span></span>
<span data-ttu-id="c71ba-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="c71ba-118">This parameter is required.</span></span>

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

### <span data-ttu-id="c71ba-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c71ba-119">CommonParameters</span></span>
<span data-ttu-id="c71ba-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c71ba-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c71ba-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c71ba-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c71ba-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c71ba-122">INPUTS</span></span>

### <span data-ttu-id="c71ba-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c71ba-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c71ba-124">System.String</span><span class="sxs-lookup"><span data-stu-id="c71ba-124">System.String</span></span>

## <span data-ttu-id="c71ba-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c71ba-125">OUTPUTS</span></span>

### <span data-ttu-id="c71ba-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c71ba-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="c71ba-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c71ba-127">NOTES</span></span>

## <span data-ttu-id="c71ba-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c71ba-128">RELATED LINKS</span></span>
