---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserverclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
ms.openlocfilehash: 19e49269a4ae07b39e7a2795636e51df75b54905
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205831"
---
# <span data-ttu-id="ab596-101">Get-AzApiManagementAuthorizationServerClientSecret</span><span class="sxs-lookup"><span data-stu-id="ab596-101">Get-AzApiManagementAuthorizationServerClientSecret</span></span>

## <span data-ttu-id="ab596-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab596-102">SYNOPSIS</span></span>
<span data-ttu-id="ab596-103">Api Management authorization server client secret (API Management authorization server client secret) kap.</span><span class="sxs-lookup"><span data-stu-id="ab596-103">Gets an API Management authorization server client secret.</span></span>

## <span data-ttu-id="ab596-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ab596-104">SYNTAX</span></span>

### <span data-ttu-id="ab596-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab596-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab596-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab596-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab596-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ab596-107">DESCRIPTION</span></span>
<span data-ttu-id="ab596-108">A **Get-AzApiManagementAuthorizationServerClientSecret** parancsmag az Azure API Management engedélyezési kiszolgálójának ügyféltitkját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ab596-108">The **Get-AzApiManagementAuthorizationServerClientSecret** cmdlet gets the client secret of the Azure API Management authorization server.</span></span>

## <span data-ttu-id="ab596-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ab596-109">EXAMPLES</span></span>

### <span data-ttu-id="ab596-110">1. példa: Egy megadott engedélyezési kiszolgáló ügyfélprogram-titkos kódjának lekérte azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="ab596-110">Example 1: Get a specified authorization server client secret by id</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServerClientSecret -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="ab596-111">Ez a parancs megkapja a megadott engedélyezési kiszolgáló cient-titkos nevét.</span><span class="sxs-lookup"><span data-stu-id="ab596-111">This command gets the specified authorization server cient secret.</span></span>

## <span data-ttu-id="ab596-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab596-112">PARAMETERS</span></span>

### <span data-ttu-id="ab596-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ab596-113">-Context</span></span>
<span data-ttu-id="ab596-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="ab596-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ab596-115">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="ab596-115">This parameter is required.</span></span>

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

### <span data-ttu-id="ab596-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab596-116">-DefaultProfile</span></span>
<span data-ttu-id="ab596-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab596-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab596-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab596-118">-ResourceId</span></span>
<span data-ttu-id="ab596-119">Az engedélyezési kiszolgáló erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ab596-119">Arm Resource Identifier of the authorization server.</span></span>
<span data-ttu-id="ab596-120">Ha meg van adva, a rendszer megpróbálja megtalálni az engedélyezési kiszolgálót az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="ab596-120">If specified will try to find authorization server by the identifier.</span></span>
<span data-ttu-id="ab596-121">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="ab596-121">This parameter is required.</span></span>

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

### <span data-ttu-id="ab596-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="ab596-122">-ServerId</span></span>
<span data-ttu-id="ab596-123">Az engedélyezési kiszolgáló azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ab596-123">Identifier of the authorization server.</span></span>
<span data-ttu-id="ab596-124">Ha meg van adva, az engedélyezési kiszolgálót az azonosító alapján fogja megtalálni.</span><span class="sxs-lookup"><span data-stu-id="ab596-124">If specified will find authorization server by the identifier.</span></span>
<span data-ttu-id="ab596-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ab596-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab596-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab596-126">CommonParameters</span></span>
<span data-ttu-id="ab596-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab596-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab596-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab596-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab596-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab596-129">INPUTS</span></span>

### <span data-ttu-id="ab596-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ab596-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ab596-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ab596-131">System.String</span></span>

## <span data-ttu-id="ab596-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab596-132">OUTPUTS</span></span>

### <span data-ttu-id="ab596-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="ab596-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="ab596-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ab596-134">NOTES</span></span>

## <span data-ttu-id="ab596-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab596-135">RELATED LINKS</span></span>
