---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: ea9975038f1c738461f8c3bbda4cba70bafe8ad9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920866"
---
# <span data-ttu-id="47603-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="47603-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="47603-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47603-102">SYNOPSIS</span></span>
<span data-ttu-id="47603-103">A Backend részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="47603-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="47603-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="47603-104">SYNTAX</span></span>

### <span data-ttu-id="47603-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47603-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47603-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47603-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47603-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="47603-107">DESCRIPTION</span></span>
<span data-ttu-id="47603-108">A Backend részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="47603-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="47603-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="47603-109">EXAMPLES</span></span>

### <span data-ttu-id="47603-110">1. példa: Az összes backend lekérte</span><span class="sxs-lookup"><span data-stu-id="47603-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="47603-111">Lekérte az Api Management szolgáltatásban konfigurált összes backend-et.</span><span class="sxs-lookup"><span data-stu-id="47603-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="47603-112">2. példa: A Backend eszköznek a 123-as azonosító által megadott be szereznie</span><span class="sxs-lookup"><span data-stu-id="47603-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="47603-113">Az "123" azonosító által azonosított backend azonosító részleteinek lekérte</span><span class="sxs-lookup"><span data-stu-id="47603-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="47603-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47603-114">PARAMETERS</span></span>

### <span data-ttu-id="47603-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="47603-115">-BackendId</span></span>
<span data-ttu-id="47603-116">Egy háttér-háttér azonosítója.</span><span class="sxs-lookup"><span data-stu-id="47603-116">Identifier of a backend.</span></span>
<span data-ttu-id="47603-117">Ha meg van adva, az azonosító megpróbálja megtalálni a háttért.</span><span class="sxs-lookup"><span data-stu-id="47603-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="47603-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="47603-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="47603-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="47603-119">-Context</span></span>
<span data-ttu-id="47603-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="47603-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="47603-121">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="47603-121">This parameter is required.</span></span>

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

### <span data-ttu-id="47603-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47603-122">-DefaultProfile</span></span>
<span data-ttu-id="47603-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47603-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47603-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47603-124">-ResourceId</span></span>
<span data-ttu-id="47603-125">A háttér háttér-azonosítójának felkarolása.</span><span class="sxs-lookup"><span data-stu-id="47603-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="47603-126">Ha meg van adva, az azonosító megpróbálja megtalálni a háttért.</span><span class="sxs-lookup"><span data-stu-id="47603-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="47603-127">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="47603-127">This parameter is required.</span></span>

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

### <span data-ttu-id="47603-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47603-128">CommonParameters</span></span>
<span data-ttu-id="47603-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47603-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47603-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47603-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47603-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47603-131">INPUTS</span></span>

### <span data-ttu-id="47603-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47603-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47603-133">System.String</span><span class="sxs-lookup"><span data-stu-id="47603-133">System.String</span></span>

## <span data-ttu-id="47603-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47603-134">OUTPUTS</span></span>

### <span data-ttu-id="47603-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="47603-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="47603-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="47603-136">NOTES</span></span>

## <span data-ttu-id="47603-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47603-137">RELATED LINKS</span></span>

[<span data-ttu-id="47603-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="47603-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="47603-139">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="47603-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="47603-140">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="47603-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="47603-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="47603-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="47603-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="47603-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
