---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 4f54b361482bad24826d7120e53f96ce8d3b9eef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499288"
---
# <span data-ttu-id="763ef-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="763ef-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="763ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="763ef-102">SYNOPSIS</span></span>
<span data-ttu-id="763ef-103">Ismerje meg a backend részleteit.</span><span class="sxs-lookup"><span data-stu-id="763ef-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="763ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="763ef-104">SYNTAX</span></span>

### <span data-ttu-id="763ef-105">Az összes backend beolvasása (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="763ef-105">Get all backends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="763ef-106">Get by backend-azonosító</span><span class="sxs-lookup"><span data-stu-id="763ef-106">Get by backend ID</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="763ef-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="763ef-107">DESCRIPTION</span></span>
<span data-ttu-id="763ef-108">Ismerje meg a backend részleteit.</span><span class="sxs-lookup"><span data-stu-id="763ef-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="763ef-109">Példák</span><span class="sxs-lookup"><span data-stu-id="763ef-109">EXAMPLES</span></span>

### <span data-ttu-id="763ef-110">--------------------------Példa 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="763ef-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="763ef-111">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="763ef-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="763ef-112">Az API-kezelési szolgáltatásban konfigurált összes backend-elem listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="763ef-112">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="763ef-113">--------------------------Példa 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="763ef-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="763ef-114">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="763ef-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="763ef-115">A "123" azonosítóval azonosított megadott backend részleteinek megjelenítése</span><span class="sxs-lookup"><span data-stu-id="763ef-115">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="763ef-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="763ef-116">PARAMETERS</span></span>

### <span data-ttu-id="763ef-117">-BackendId</span><span class="sxs-lookup"><span data-stu-id="763ef-117">-BackendId</span></span>
<span data-ttu-id="763ef-118">A backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="763ef-118">Identifier of a backend.</span></span>
<span data-ttu-id="763ef-119">Ha meg van adva, a program megpróbálja megtalálni a backend-et az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="763ef-119">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="763ef-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="763ef-120">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by backend ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="763ef-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="763ef-121">-Context</span></span>
<span data-ttu-id="763ef-122">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="763ef-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="763ef-123">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="763ef-123">This parameter is required.</span></span>

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

### <span data-ttu-id="763ef-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="763ef-124">-DefaultProfile</span></span>
<span data-ttu-id="763ef-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="763ef-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="763ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="763ef-126">CommonParameters</span></span>
<span data-ttu-id="763ef-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="763ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="763ef-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="763ef-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="763ef-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="763ef-129">INPUTS</span></span>

## <span data-ttu-id="763ef-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="763ef-130">OUTPUTS</span></span>

### <span data-ttu-id="763ef-131">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend></span><span class="sxs-lookup"><span data-stu-id="763ef-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend></span></span>

### <span data-ttu-id="763ef-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementLogger. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="763ef-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger.PsApiManagementBackend</span></span>

## <span data-ttu-id="763ef-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="763ef-133">NOTES</span></span>

## <span data-ttu-id="763ef-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="763ef-134">RELATED LINKS</span></span>

[<span data-ttu-id="763ef-135">Új – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="763ef-135">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="763ef-136">Új – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="763ef-136">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="763ef-137">Új – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="763ef-137">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="763ef-138">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="763ef-138">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="763ef-139">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="763ef-139">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
