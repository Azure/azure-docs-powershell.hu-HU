---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479001"
---
# <span data-ttu-id="e0c62-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e0c62-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="e0c62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0c62-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c62-103">API-kezelési engedélyezési kiszolgálót kap.</span><span class="sxs-lookup"><span data-stu-id="e0c62-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="e0c62-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e0c62-104">SYNTAX</span></span>

### <span data-ttu-id="e0c62-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0c62-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0c62-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0c62-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0c62-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e0c62-107">DESCRIPTION</span></span>
<span data-ttu-id="e0c62-108">A **Get-AzApiManagementAuthorizationServer** parancsmag az összes Azure API Management engedélyezési kiszolgálót vagy meghatározott engedélyezési kiszolgálót megkapja.</span><span class="sxs-lookup"><span data-stu-id="e0c62-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="e0c62-109">A ClientSecret nem fog szerepelni az eredmény részletei között.</span><span class="sxs-lookup"><span data-stu-id="e0c62-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="e0c62-110">Az ügyfél titkosságának lekértelmezése: **Get-AzApiManagementAuthorizationServerClientSecret.**</span><span class="sxs-lookup"><span data-stu-id="e0c62-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="e0c62-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e0c62-111">EXAMPLES</span></span>

### <span data-ttu-id="e0c62-112">1. példa: Az összes engedélyezési kiszolgáló le kérése</span><span class="sxs-lookup"><span data-stu-id="e0c62-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="e0c62-113">Ez a parancs az összes API Management engedélyezési kiszolgálót beveszi.</span><span class="sxs-lookup"><span data-stu-id="e0c62-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="e0c62-114">2. példa: Adott engedélyezési kiszolgáló kérése</span><span class="sxs-lookup"><span data-stu-id="e0c62-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="e0c62-115">Ez a parancs a megadott engedélyezési kiszolgálót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e0c62-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="e0c62-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0c62-116">PARAMETERS</span></span>

### <span data-ttu-id="e0c62-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e0c62-117">-Context</span></span>

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

### <span data-ttu-id="e0c62-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0c62-118">-DefaultProfile</span></span>
<span data-ttu-id="e0c62-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0c62-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0c62-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0c62-120">-ResourceId</span></span>
<span data-ttu-id="e0c62-121">Az engedélyezési kiszolgáló erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e0c62-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="e0c62-122">Ha meg van adva, a rendszer megpróbálja megtalálni az engedélyezési kiszolgálót az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="e0c62-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="e0c62-123">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="e0c62-123">This parameter is required.</span></span>

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

### <span data-ttu-id="e0c62-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="e0c62-124">-ServerId</span></span>
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

### <span data-ttu-id="e0c62-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c62-125">CommonParameters</span></span>
<span data-ttu-id="e0c62-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0c62-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c62-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0c62-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c62-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0c62-128">INPUTS</span></span>

### <span data-ttu-id="e0c62-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e0c62-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e0c62-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e0c62-130">System.String</span></span>

## <span data-ttu-id="e0c62-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0c62-131">OUTPUTS</span></span>

### <span data-ttu-id="e0c62-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e0c62-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="e0c62-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e0c62-133">NOTES</span></span>

## <span data-ttu-id="e0c62-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0c62-134">RELATED LINKS</span></span>

[<span data-ttu-id="e0c62-135">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e0c62-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="e0c62-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e0c62-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="e0c62-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e0c62-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


