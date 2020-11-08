---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187890"
---
# <span data-ttu-id="23206-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="23206-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="23206-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23206-102">SYNOPSIS</span></span>
<span data-ttu-id="23206-103">Ismerje meg a backend részleteit.</span><span class="sxs-lookup"><span data-stu-id="23206-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="23206-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23206-104">SYNTAX</span></span>

### <span data-ttu-id="23206-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23206-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23206-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23206-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23206-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="23206-107">DESCRIPTION</span></span>
<span data-ttu-id="23206-108">Ismerje meg a backend részleteit.</span><span class="sxs-lookup"><span data-stu-id="23206-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="23206-109">Példák</span><span class="sxs-lookup"><span data-stu-id="23206-109">EXAMPLES</span></span>

### <span data-ttu-id="23206-110">Példa 1: az összes backend beolvasása</span><span class="sxs-lookup"><span data-stu-id="23206-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="23206-111">Az API-kezelési szolgáltatásban konfigurált összes backend-elem listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="23206-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="23206-112">2. példa: a 123 azonosítóval megadott backend beolvasása</span><span class="sxs-lookup"><span data-stu-id="23206-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="23206-113">A "123" azonosítóval azonosított megadott backend részleteinek megjelenítése</span><span class="sxs-lookup"><span data-stu-id="23206-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="23206-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23206-114">PARAMETERS</span></span>

### <span data-ttu-id="23206-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="23206-115">-BackendId</span></span>
<span data-ttu-id="23206-116">A backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="23206-116">Identifier of a backend.</span></span>
<span data-ttu-id="23206-117">Ha meg van adva, a program megpróbálja megtalálni a backend-et az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="23206-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="23206-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="23206-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="23206-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="23206-119">-Context</span></span>
<span data-ttu-id="23206-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="23206-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="23206-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="23206-121">This parameter is required.</span></span>

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

### <span data-ttu-id="23206-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23206-122">-DefaultProfile</span></span>
<span data-ttu-id="23206-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23206-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23206-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23206-124">-ResourceId</span></span>
<span data-ttu-id="23206-125">A háttér ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="23206-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="23206-126">Ha meg van adva, a program megpróbálja megtalálni a backend-et az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="23206-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="23206-127">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="23206-127">This parameter is required.</span></span>

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

### <span data-ttu-id="23206-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23206-128">CommonParameters</span></span>
<span data-ttu-id="23206-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23206-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23206-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="23206-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23206-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23206-131">INPUTS</span></span>

### <span data-ttu-id="23206-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="23206-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="23206-133">System. String</span><span class="sxs-lookup"><span data-stu-id="23206-133">System.String</span></span>

## <span data-ttu-id="23206-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23206-134">OUTPUTS</span></span>

### <span data-ttu-id="23206-135">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="23206-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="23206-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23206-136">NOTES</span></span>

## <span data-ttu-id="23206-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23206-137">RELATED LINKS</span></span>

[<span data-ttu-id="23206-138">Új – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="23206-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="23206-139">Új – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="23206-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="23206-140">Új – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="23206-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="23206-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="23206-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="23206-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="23206-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
