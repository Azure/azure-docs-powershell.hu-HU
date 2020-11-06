---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 11d832bc74aca4ac274ee17ff0b38de06b77e377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494233"
---
# <span data-ttu-id="d85f5-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d85f5-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="d85f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d85f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d85f5-103">Ismerje meg a backend részleteit.</span><span class="sxs-lookup"><span data-stu-id="d85f5-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d85f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d85f5-104">SYNTAX</span></span>

### <span data-ttu-id="d85f5-105">GetAllBackends (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d85f5-105">GetAllBackends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d85f5-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="d85f5-106">GetByBackendId</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d85f5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d85f5-107">DESCRIPTION</span></span>
<span data-ttu-id="d85f5-108">Ismerje meg a backend részleteit.</span><span class="sxs-lookup"><span data-stu-id="d85f5-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="d85f5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d85f5-109">EXAMPLES</span></span>

### <span data-ttu-id="d85f5-110">Példa 1: az összes backend beolvasása</span><span class="sxs-lookup"><span data-stu-id="d85f5-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="d85f5-111">Az API-kezelési szolgáltatásban konfigurált összes backend-elem listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="d85f5-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="d85f5-112">2. példa: a 123 azonosítóval megadott backend beolvasása</span><span class="sxs-lookup"><span data-stu-id="d85f5-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="d85f5-113">A "123" azonosítóval azonosított megadott backend részleteinek megjelenítése</span><span class="sxs-lookup"><span data-stu-id="d85f5-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="d85f5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d85f5-114">PARAMETERS</span></span>

### <span data-ttu-id="d85f5-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="d85f5-115">-BackendId</span></span>
<span data-ttu-id="d85f5-116">A backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d85f5-116">Identifier of a backend.</span></span>
<span data-ttu-id="d85f5-117">Ha meg van adva, a program megpróbálja megtalálni a backend-et az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="d85f5-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="d85f5-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="d85f5-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByBackendId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d85f5-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d85f5-119">-Context</span></span>
<span data-ttu-id="d85f5-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="d85f5-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d85f5-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="d85f5-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d85f5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85f5-122">-DefaultProfile</span></span>
<span data-ttu-id="d85f5-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d85f5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85f5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85f5-124">CommonParameters</span></span>
<span data-ttu-id="d85f5-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d85f5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85f5-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d85f5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85f5-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d85f5-127">INPUTS</span></span>

### <span data-ttu-id="d85f5-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d85f5-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d85f5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d85f5-129">System.String</span></span>

## <span data-ttu-id="d85f5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d85f5-130">OUTPUTS</span></span>

### <span data-ttu-id="d85f5-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d85f5-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="d85f5-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d85f5-132">NOTES</span></span>

## <span data-ttu-id="d85f5-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d85f5-133">RELATED LINKS</span></span>

[<span data-ttu-id="d85f5-134">Új – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d85f5-134">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="d85f5-135">Új – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d85f5-135">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="d85f5-136">Új – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d85f5-136">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="d85f5-137">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d85f5-137">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="d85f5-138">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d85f5-138">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
