---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302252"
---
# <span data-ttu-id="cc27b-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="cc27b-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="cc27b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc27b-102">SYNOPSIS</span></span>
<span data-ttu-id="cc27b-103">API-kezelési engedélyezési kiszolgáló kapja.</span><span class="sxs-lookup"><span data-stu-id="cc27b-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="cc27b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc27b-104">SYNTAX</span></span>

### <span data-ttu-id="cc27b-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc27b-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc27b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc27b-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc27b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc27b-107">DESCRIPTION</span></span>
<span data-ttu-id="cc27b-108">A **Get-AzApiManagementAuthorizationServer** parancsmag minden Azure API-kezelési engedélyezési kiszolgálót vagy megadott engedélyezési kiszolgálót kap.</span><span class="sxs-lookup"><span data-stu-id="cc27b-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="cc27b-109">A ClientSecret nem fog szerepelni az eredmény részletei között.</span><span class="sxs-lookup"><span data-stu-id="cc27b-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="cc27b-110">Az ügyfél titkának beszerzéséhez használja a **Get-AzApiManagementAuthorizationServerClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="cc27b-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="cc27b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cc27b-111">EXAMPLES</span></span>

### <span data-ttu-id="cc27b-112">1. példa: az összes engedélyezési kiszolgáló beszerzése</span><span class="sxs-lookup"><span data-stu-id="cc27b-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="cc27b-113">Ez a parancs minden API-kezelési engedélyezési kiszolgálót beolvassa.</span><span class="sxs-lookup"><span data-stu-id="cc27b-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="cc27b-114">2. példa: meghatározott engedélyezési kiszolgáló beszerzése</span><span class="sxs-lookup"><span data-stu-id="cc27b-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="cc27b-115">Ez a parancs a megadott engedélyezési kiszolgálót kapja.</span><span class="sxs-lookup"><span data-stu-id="cc27b-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="cc27b-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc27b-116">PARAMETERS</span></span>

### <span data-ttu-id="cc27b-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="cc27b-117">-Context</span></span>

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

### <span data-ttu-id="cc27b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc27b-118">-DefaultProfile</span></span>
<span data-ttu-id="cc27b-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc27b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc27b-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc27b-120">-ResourceId</span></span>
<span data-ttu-id="cc27b-121">Az engedélyezési kiszolgáló ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cc27b-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="cc27b-122">Ha meg van adva, az azonosító alapján megpróbálja megtalálni az engedélyezési kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="cc27b-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="cc27b-123">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cc27b-123">This parameter is required.</span></span>

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

### <span data-ttu-id="cc27b-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="cc27b-124">-ServerId</span></span>
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

### <span data-ttu-id="cc27b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc27b-125">CommonParameters</span></span>
<span data-ttu-id="cc27b-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc27b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc27b-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cc27b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc27b-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc27b-128">INPUTS</span></span>

### <span data-ttu-id="cc27b-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cc27b-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cc27b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cc27b-130">System.String</span></span>

## <span data-ttu-id="cc27b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc27b-131">OUTPUTS</span></span>

### <span data-ttu-id="cc27b-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="cc27b-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="cc27b-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc27b-133">NOTES</span></span>

## <span data-ttu-id="cc27b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc27b-134">RELATED LINKS</span></span>

[<span data-ttu-id="cc27b-135">Új – AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="cc27b-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="cc27b-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="cc27b-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="cc27b-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="cc27b-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


