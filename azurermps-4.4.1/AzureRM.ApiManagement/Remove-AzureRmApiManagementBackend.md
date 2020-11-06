---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 03f56a17d038407b3a33c09188c9a29b6f4caf09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493897"
---
# <span data-ttu-id="a111e-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a111e-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="a111e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a111e-102">SYNOPSIS</span></span>
<span data-ttu-id="a111e-103">A backend eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a111e-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a111e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a111e-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a111e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a111e-105">DESCRIPTION</span></span>
<span data-ttu-id="a111e-106">Eltávolítja az azonosító által az API-menedzsment által megadott hátteret.</span><span class="sxs-lookup"><span data-stu-id="a111e-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="a111e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a111e-107">EXAMPLES</span></span>

### <span data-ttu-id="a111e-108">1. példa: a backend 123 eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a111e-108">Example 1: Remove the Backend 123</span></span>
```
Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="a111e-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a111e-109">PARAMETERS</span></span>

### <span data-ttu-id="a111e-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="a111e-110">-BackendId</span></span>
<span data-ttu-id="a111e-111">A meglévő backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a111e-111">Identifier of existing backend.</span></span>
<span data-ttu-id="a111e-112">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a111e-112">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a111e-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a111e-113">-Context</span></span>
<span data-ttu-id="a111e-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="a111e-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a111e-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a111e-115">This parameter is required.</span></span>

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

### <span data-ttu-id="a111e-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a111e-116">-PassThru</span></span>
<span data-ttu-id="a111e-117">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="a111e-117">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="a111e-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="a111e-118">This parameter is optional.</span></span>
<span data-ttu-id="a111e-119">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="a111e-119">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a111e-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a111e-120">-Confirm</span></span>
<span data-ttu-id="a111e-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a111e-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a111e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a111e-122">-WhatIf</span></span>
<span data-ttu-id="a111e-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a111e-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a111e-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a111e-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a111e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a111e-125">-DefaultProfile</span></span>
<span data-ttu-id="a111e-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a111e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a111e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a111e-127">CommonParameters</span></span>
<span data-ttu-id="a111e-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a111e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a111e-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a111e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a111e-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a111e-130">INPUTS</span></span>

## <span data-ttu-id="a111e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a111e-131">OUTPUTS</span></span>

### <span data-ttu-id="a111e-132">bool</span><span class="sxs-lookup"><span data-stu-id="a111e-132">bool</span></span>

## <span data-ttu-id="a111e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a111e-133">NOTES</span></span>

## <span data-ttu-id="a111e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a111e-134">RELATED LINKS</span></span>

[<span data-ttu-id="a111e-135">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a111e-135">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="a111e-136">Új – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a111e-136">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="a111e-137">Új – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a111e-137">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="a111e-138">Új – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a111e-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="a111e-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a111e-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
