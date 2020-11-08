---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserverclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
ms.openlocfilehash: 19e49269a4ae07b39e7a2795636e51df75b54905
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183402"
---
# <span data-ttu-id="020a2-101">Get-AzApiManagementAuthorizationServerClientSecret</span><span class="sxs-lookup"><span data-stu-id="020a2-101">Get-AzApiManagementAuthorizationServerClientSecret</span></span>

## <span data-ttu-id="020a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="020a2-102">SYNOPSIS</span></span>
<span data-ttu-id="020a2-103">Megkapja az API-kezelés engedélyezési kiszolgálójának az ügyfél titkát.</span><span class="sxs-lookup"><span data-stu-id="020a2-103">Gets an API Management authorization server client secret.</span></span>

## <span data-ttu-id="020a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="020a2-104">SYNTAX</span></span>

### <span data-ttu-id="020a2-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="020a2-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="020a2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="020a2-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="020a2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="020a2-107">DESCRIPTION</span></span>
<span data-ttu-id="020a2-108">A **Get-AzApiManagementAuthorizationServerClientSecret** parancsmag az Azure API-kezelés engedélyezési kiszolgálójának az ügyfél titkát kapja.</span><span class="sxs-lookup"><span data-stu-id="020a2-108">The **Get-AzApiManagementAuthorizationServerClientSecret** cmdlet gets the client secret of the Azure API Management authorization server.</span></span>

## <span data-ttu-id="020a2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="020a2-109">EXAMPLES</span></span>

### <span data-ttu-id="020a2-110">Példa 1: meghatározott engedélyezési kiszolgáló-ügyfél titkos azonosítójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="020a2-110">Example 1: Get a specified authorization server client secret by id</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServerClientSecret -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="020a2-111">Ez a parancs a megadott engedélyezési kiszolgáló titkát kapja.</span><span class="sxs-lookup"><span data-stu-id="020a2-111">This command gets the specified authorization server cient secret.</span></span>

## <span data-ttu-id="020a2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="020a2-112">PARAMETERS</span></span>

### <span data-ttu-id="020a2-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="020a2-113">-Context</span></span>
<span data-ttu-id="020a2-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="020a2-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="020a2-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="020a2-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="020a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020a2-116">-DefaultProfile</span></span>
<span data-ttu-id="020a2-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="020a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="020a2-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="020a2-118">-ResourceId</span></span>
<span data-ttu-id="020a2-119">Az engedélyezési kiszolgáló ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="020a2-119">Arm Resource Identifier of the authorization server.</span></span>
<span data-ttu-id="020a2-120">Ha meg van adva, az azonosító alapján megpróbálja megtalálni az engedélyezési kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="020a2-120">If specified will try to find authorization server by the identifier.</span></span>
<span data-ttu-id="020a2-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="020a2-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="020a2-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="020a2-122">-ServerId</span></span>
<span data-ttu-id="020a2-123">Az engedélyezési kiszolgáló azonosítója.</span><span class="sxs-lookup"><span data-stu-id="020a2-123">Identifier of the authorization server.</span></span>
<span data-ttu-id="020a2-124">Ha meg van adva az engedélyezési kiszolgáló, az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="020a2-124">If specified will find authorization server by the identifier.</span></span>
<span data-ttu-id="020a2-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="020a2-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="020a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020a2-126">CommonParameters</span></span>
<span data-ttu-id="020a2-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="020a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020a2-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="020a2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020a2-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="020a2-129">INPUTS</span></span>

### <span data-ttu-id="020a2-130">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="020a2-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="020a2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="020a2-131">System.String</span></span>

## <span data-ttu-id="020a2-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="020a2-132">OUTPUTS</span></span>

### <span data-ttu-id="020a2-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="020a2-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="020a2-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="020a2-134">NOTES</span></span>

## <span data-ttu-id="020a2-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="020a2-135">RELATED LINKS</span></span>
