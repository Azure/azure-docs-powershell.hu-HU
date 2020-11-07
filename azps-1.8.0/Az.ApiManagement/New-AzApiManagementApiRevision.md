---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 81a80acdfb89f30cc1add6b1cfc10bcd7d745dfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665646"
---
# <span data-ttu-id="e25a9-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="e25a9-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="e25a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e25a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e25a9-103">Egy meglévő API új verzióját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e25a9-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="e25a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e25a9-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e25a9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e25a9-105">DESCRIPTION</span></span>

<span data-ttu-id="e25a9-106">A **New-AzApiManagementApiRevision** parancsmag létrehoz egy API-verziót az API-kezelési környezet meglévő API-hoz.</span><span class="sxs-lookup"><span data-stu-id="e25a9-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="e25a9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e25a9-107">EXAMPLES</span></span>

### <span data-ttu-id="e25a9-108">1. példa: API-módosítás létrehozása API-hoz</span><span class="sxs-lookup"><span data-stu-id="e25a9-108">Example 1: Create an API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $ApiMgmtContext  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6


ApiId                         : 5adf6fbf0faadf3ad8558065;rev=6
Name                          : httpbin.org
Description                   : API Management facade for a very handy and free online HTTP tool.
ServiceUrl                    : https://httpbin.org/
Path                          : httpbin
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         : contoso-oauth
AuthorizationScope            : contoso-oauth
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 6
ApiVersion                    : v1
IsCurrent                     : False
IsOnline                      : False
Id                            : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065;rev=6
ResourceGroupName             : Api-Default-WestUS
ServiceName                   : contoso
```

<span data-ttu-id="e25a9-109">Ez a parancs az API API-változatát hozza létre `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="e25a9-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

## <span data-ttu-id="e25a9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e25a9-110">PARAMETERS</span></span>

### <span data-ttu-id="e25a9-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e25a9-111">-ApiId</span></span>
<span data-ttu-id="e25a9-112">Annak az API-nek az azonosítója, amelynek a módosítását létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="e25a9-112">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="e25a9-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e25a9-113">-ApiRevision</span></span>
<span data-ttu-id="e25a9-114">Az API verziószámának azonosítója</span><span class="sxs-lookup"><span data-stu-id="e25a9-114">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="e25a9-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e25a9-115">-Context</span></span>
<span data-ttu-id="e25a9-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="e25a9-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e25a9-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="e25a9-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e25a9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e25a9-118">-DefaultProfile</span></span>
<span data-ttu-id="e25a9-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e25a9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e25a9-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e25a9-120">-Confirm</span></span>
<span data-ttu-id="e25a9-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e25a9-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25a9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e25a9-122">-WhatIf</span></span>
<span data-ttu-id="e25a9-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e25a9-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e25a9-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e25a9-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25a9-125">CommonParameters</span></span>
<span data-ttu-id="e25a9-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e25a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25a9-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e25a9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25a9-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e25a9-128">INPUTS</span></span>

### <span data-ttu-id="e25a9-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e25a9-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e25a9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e25a9-130">System.String</span></span>

## <span data-ttu-id="e25a9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e25a9-131">OUTPUTS</span></span>

### <span data-ttu-id="e25a9-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e25a9-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="e25a9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e25a9-133">NOTES</span></span>

## <span data-ttu-id="e25a9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e25a9-134">RELATED LINKS</span></span>

[<span data-ttu-id="e25a9-135">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e25a9-135">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="e25a9-136">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e25a9-136">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="e25a9-137">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e25a9-137">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
