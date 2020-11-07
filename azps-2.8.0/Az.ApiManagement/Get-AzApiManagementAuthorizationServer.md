---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ce401334b03620ac565c5dd3b737b7a2982575e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668122"
---
# <span data-ttu-id="7fbd3-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7fbd3-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="7fbd3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7fbd3-102">SYNOPSIS</span></span>
<span data-ttu-id="7fbd3-103">API-kezelési engedélyezési kiszolgáló kapja.</span><span class="sxs-lookup"><span data-stu-id="7fbd3-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="7fbd3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7fbd3-104">SYNTAX</span></span>

### <span data-ttu-id="7fbd3-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7fbd3-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fbd3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fbd3-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fbd3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7fbd3-107">DESCRIPTION</span></span>
<span data-ttu-id="7fbd3-108">A **Get-AzApiManagementAuthorizationServer** parancsmag minden Azure API-kezelési engedélyezési kiszolgálót vagy megadott engedélyezési kiszolgálót kap.</span><span class="sxs-lookup"><span data-stu-id="7fbd3-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="7fbd3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7fbd3-109">EXAMPLES</span></span>

### <span data-ttu-id="7fbd3-110">1. példa: az összes engedélyezési kiszolgáló beszerzése</span><span class="sxs-lookup"><span data-stu-id="7fbd3-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="7fbd3-111">Ez a parancs minden API-kezelési engedélyezési kiszolgálót beolvassa.</span><span class="sxs-lookup"><span data-stu-id="7fbd3-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="7fbd3-112">2. példa: meghatározott engedélyezési kiszolgáló beszerzése</span><span class="sxs-lookup"><span data-stu-id="7fbd3-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="7fbd3-113">Ez a parancs a megadott engedélyezési kiszolgálót kapja.</span><span class="sxs-lookup"><span data-stu-id="7fbd3-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="7fbd3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7fbd3-114">PARAMETERS</span></span>

### <span data-ttu-id="7fbd3-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7fbd3-115">-Context</span></span>

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

### <span data-ttu-id="7fbd3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fbd3-116">-DefaultProfile</span></span>
<span data-ttu-id="7fbd3-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7fbd3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fbd3-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fbd3-118">-ResourceId</span></span>
<span data-ttu-id="7fbd3-119">Az engedélyezési kiszolgáló ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7fbd3-119">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="7fbd3-120">Ha meg van adva, az azonosító alapján megpróbálja megtalálni az engedélyezési kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="7fbd3-120">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="7fbd3-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="7fbd3-121">This parameter is required.</span></span>

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

### <span data-ttu-id="7fbd3-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="7fbd3-122">-ServerId</span></span>
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

### <span data-ttu-id="7fbd3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fbd3-123">CommonParameters</span></span>
<span data-ttu-id="7fbd3-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7fbd3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fbd3-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7fbd3-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fbd3-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fbd3-126">INPUTS</span></span>

### <span data-ttu-id="7fbd3-127">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7fbd3-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7fbd3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7fbd3-128">System.String</span></span>

## <span data-ttu-id="7fbd3-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fbd3-129">OUTPUTS</span></span>

### <span data-ttu-id="7fbd3-130">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7fbd3-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="7fbd3-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7fbd3-131">NOTES</span></span>

## <span data-ttu-id="7fbd3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fbd3-132">RELATED LINKS</span></span>

[<span data-ttu-id="7fbd3-133">Új – AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7fbd3-133">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="7fbd3-134">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7fbd3-134">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="7fbd3-135">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7fbd3-135">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


