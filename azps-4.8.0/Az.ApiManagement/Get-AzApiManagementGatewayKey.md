---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025607"
---
# <span data-ttu-id="c6f4f-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c6f4f-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="c6f4f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f4f-103">A meglévő átjáró kulcsait kapja</span><span class="sxs-lookup"><span data-stu-id="c6f4f-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="c6f4f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6f4f-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6f4f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6f4f-105">DESCRIPTION</span></span>
<span data-ttu-id="c6f4f-106">A **Get-AzApiManagementGatewayKey** parancsmag a meglévő átjáró kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="c6f4f-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="c6f4f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c6f4f-107">EXAMPLES</span></span>

### <span data-ttu-id="c6f4f-108">2. példa: átjáró beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="c6f4f-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="c6f4f-109">Ez a parancs a "0123456789" átjáró kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c6f4f-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="c6f4f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6f4f-110">PARAMETERS</span></span>

### <span data-ttu-id="c6f4f-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c6f4f-111">-Context</span></span>
<span data-ttu-id="c6f4f-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="c6f4f-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c6f4f-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="c6f4f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="c6f4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f4f-114">-DefaultProfile</span></span>
<span data-ttu-id="c6f4f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6f4f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6f4f-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="c6f4f-116">-GatewayId</span></span>
<span data-ttu-id="c6f4f-117">Átjáró-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c6f4f-117">Gateway identifier.</span></span>
<span data-ttu-id="c6f4f-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="c6f4f-118">This parameter is required.</span></span>

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

### <span data-ttu-id="c6f4f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f4f-119">CommonParameters</span></span>
<span data-ttu-id="c6f4f-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6f4f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f4f-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c6f4f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f4f-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6f4f-122">INPUTS</span></span>

### <span data-ttu-id="c6f4f-123">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c6f4f-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c6f4f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c6f4f-124">System.String</span></span>

## <span data-ttu-id="c6f4f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6f4f-125">OUTPUTS</span></span>

### <span data-ttu-id="c6f4f-126">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c6f4f-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="c6f4f-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6f4f-127">NOTES</span></span>

## <span data-ttu-id="c6f4f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6f4f-128">RELATED LINKS</span></span>
