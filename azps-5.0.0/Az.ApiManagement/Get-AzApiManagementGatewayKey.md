---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299906"
---
# <span data-ttu-id="97623-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="97623-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="97623-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97623-102">SYNOPSIS</span></span>
<span data-ttu-id="97623-103">A meglévő átjáró kulcsait kapja</span><span class="sxs-lookup"><span data-stu-id="97623-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="97623-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97623-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97623-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97623-105">DESCRIPTION</span></span>
<span data-ttu-id="97623-106">A **Get-AzApiManagementGatewayKey** parancsmag a meglévő átjáró kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="97623-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="97623-107">Példák</span><span class="sxs-lookup"><span data-stu-id="97623-107">EXAMPLES</span></span>

### <span data-ttu-id="97623-108">2. példa: átjáró beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="97623-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="97623-109">Ez a parancs a "0123456789" átjáró kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="97623-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="97623-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97623-110">PARAMETERS</span></span>

### <span data-ttu-id="97623-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="97623-111">-Context</span></span>
<span data-ttu-id="97623-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="97623-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="97623-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="97623-113">This parameter is required.</span></span>

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

### <span data-ttu-id="97623-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97623-114">-DefaultProfile</span></span>
<span data-ttu-id="97623-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97623-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97623-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="97623-116">-GatewayId</span></span>
<span data-ttu-id="97623-117">Átjáró-azonosító.</span><span class="sxs-lookup"><span data-stu-id="97623-117">Gateway identifier.</span></span>
<span data-ttu-id="97623-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="97623-118">This parameter is required.</span></span>

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

### <span data-ttu-id="97623-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97623-119">CommonParameters</span></span>
<span data-ttu-id="97623-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97623-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97623-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="97623-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97623-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97623-122">INPUTS</span></span>

### <span data-ttu-id="97623-123">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="97623-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="97623-124">System. String</span><span class="sxs-lookup"><span data-stu-id="97623-124">System.String</span></span>

## <span data-ttu-id="97623-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97623-125">OUTPUTS</span></span>

### <span data-ttu-id="97623-126">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="97623-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="97623-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97623-127">NOTES</span></span>

## <span data-ttu-id="97623-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97623-128">RELATED LINKS</span></span>
