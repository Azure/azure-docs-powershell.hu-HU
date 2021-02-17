---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205822"
---
# <span data-ttu-id="e56c2-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e56c2-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="e56c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e56c2-102">SYNOPSIS</span></span>
<span data-ttu-id="e56c2-103">A Backend részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="e56c2-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="e56c2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e56c2-104">SYNTAX</span></span>

### <span data-ttu-id="e56c2-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e56c2-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e56c2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e56c2-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e56c2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e56c2-107">DESCRIPTION</span></span>
<span data-ttu-id="e56c2-108">A Backend részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="e56c2-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="e56c2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e56c2-109">EXAMPLES</span></span>

### <span data-ttu-id="e56c2-110">1. példa: Az összes backend lekérte</span><span class="sxs-lookup"><span data-stu-id="e56c2-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="e56c2-111">Lekérte az Api Management szolgáltatásban konfigurált összes backend-et.</span><span class="sxs-lookup"><span data-stu-id="e56c2-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="e56c2-112">2. példa: A Backend eszköz 123 azonosító által megadott be szereznie</span><span class="sxs-lookup"><span data-stu-id="e56c2-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="e56c2-113">Az "123" azonosító által azonosított backend azonosító részleteinek lekérte</span><span class="sxs-lookup"><span data-stu-id="e56c2-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="e56c2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e56c2-114">PARAMETERS</span></span>

### <span data-ttu-id="e56c2-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="e56c2-115">-BackendId</span></span>
<span data-ttu-id="e56c2-116">Egy háttér-háttér azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e56c2-116">Identifier of a backend.</span></span>
<span data-ttu-id="e56c2-117">Ha meg van adva, az azonosító megpróbálja megtalálni a háttért.</span><span class="sxs-lookup"><span data-stu-id="e56c2-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="e56c2-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e56c2-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="e56c2-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e56c2-119">-Context</span></span>
<span data-ttu-id="e56c2-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="e56c2-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e56c2-121">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="e56c2-121">This parameter is required.</span></span>

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

### <span data-ttu-id="e56c2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e56c2-122">-DefaultProfile</span></span>
<span data-ttu-id="e56c2-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e56c2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e56c2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e56c2-124">-ResourceId</span></span>
<span data-ttu-id="e56c2-125">A háttér háttér-azonosítójának felkarolása.</span><span class="sxs-lookup"><span data-stu-id="e56c2-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="e56c2-126">Ha meg van adva, az azonosító megpróbálja megtalálni a háttért.</span><span class="sxs-lookup"><span data-stu-id="e56c2-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="e56c2-127">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="e56c2-127">This parameter is required.</span></span>

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

### <span data-ttu-id="e56c2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e56c2-128">CommonParameters</span></span>
<span data-ttu-id="e56c2-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e56c2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e56c2-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e56c2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e56c2-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e56c2-131">INPUTS</span></span>

### <span data-ttu-id="e56c2-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e56c2-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e56c2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e56c2-133">System.String</span></span>

## <span data-ttu-id="e56c2-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e56c2-134">OUTPUTS</span></span>

### <span data-ttu-id="e56c2-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e56c2-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="e56c2-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e56c2-136">NOTES</span></span>

## <span data-ttu-id="e56c2-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e56c2-137">RELATED LINKS</span></span>

[<span data-ttu-id="e56c2-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e56c2-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="e56c2-139">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e56c2-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="e56c2-140">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e56c2-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="e56c2-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e56c2-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="e56c2-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e56c2-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
