---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: cb7fbfe4ba4fdf09b9012ddc5be8028af0bd80c1
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93506044"
---
# <span data-ttu-id="d8a18-101">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d8a18-101">New-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="d8a18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8a18-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a18-103">API-kiadás API-változatának létrehozása</span><span class="sxs-lookup"><span data-stu-id="d8a18-103">Creates an API Release of an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8a18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8a18-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8a18-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8a18-105">DESCRIPTION</span></span>

<span data-ttu-id="d8a18-106">A **New-AzureRmApiManagementApiRelease** parancsmag API-kiadást hoz létre az API-kezelési környezet API-verziójában.</span><span class="sxs-lookup"><span data-stu-id="d8a18-106">The **New-AzureRmApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="d8a18-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d8a18-107">EXAMPLES</span></span>

### <span data-ttu-id="d8a18-108">1. példa: API-kiadás létrehozása API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="d8a18-108">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


ReleaseId         : 7e4d3fbb43c146c4bf406499ef9411f4
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 1:16:29 AM
UpdatedDateTime   : 5/17/2018 1:16:29 AM
Notes             : Releasing version 6
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/7e4d3fbb43c146c4bf40649
                    9ef9411f4
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="d8a18-109">Ez a parancs API-kiadást hoz létre `2` a módosítások számára `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="d8a18-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="d8a18-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8a18-110">PARAMETERS</span></span>

### <span data-ttu-id="d8a18-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d8a18-111">-ApiId</span></span>
<span data-ttu-id="d8a18-112">Azonosítót az új API-hoz.</span><span class="sxs-lookup"><span data-stu-id="d8a18-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="d8a18-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d8a18-113">-ApiRevision</span></span>
<span data-ttu-id="d8a18-114">Az API-módosítás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d8a18-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="d8a18-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d8a18-115">-Context</span></span>
<span data-ttu-id="d8a18-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="d8a18-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d8a18-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="d8a18-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a18-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a18-118">-DefaultProfile</span></span>
<span data-ttu-id="d8a18-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8a18-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8a18-120">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="d8a18-120">-Note</span></span>
<span data-ttu-id="d8a18-121">API-kibocsátási megjegyzések.</span><span class="sxs-lookup"><span data-stu-id="d8a18-121">Api Release Notes.</span></span> <span data-ttu-id="d8a18-122">Ez a paraméter nem kötelező</span><span class="sxs-lookup"><span data-stu-id="d8a18-122">This parameter is optional</span></span>

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

### <span data-ttu-id="d8a18-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="d8a18-123">-ReleaseId</span></span>
<span data-ttu-id="d8a18-124">Az API-kiadás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d8a18-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="d8a18-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="d8a18-125">This parameter is optional.</span></span>
<span data-ttu-id="d8a18-126">Ha a program nem hoz létre megadott azonosítót.</span><span class="sxs-lookup"><span data-stu-id="d8a18-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="d8a18-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d8a18-127">-Confirm</span></span>
<span data-ttu-id="d8a18-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d8a18-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8a18-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8a18-129">-WhatIf</span></span>
<span data-ttu-id="d8a18-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d8a18-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8a18-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8a18-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8a18-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a18-132">CommonParameters</span></span>
<span data-ttu-id="d8a18-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8a18-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a18-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8a18-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a18-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8a18-135">INPUTS</span></span>

### <span data-ttu-id="d8a18-136">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d8a18-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="d8a18-137">Paraméterek: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d8a18-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="d8a18-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d8a18-138">System.String</span></span>

## <span data-ttu-id="d8a18-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8a18-139">OUTPUTS</span></span>

### <span data-ttu-id="d8a18-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d8a18-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="d8a18-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8a18-141">NOTES</span></span>

## <span data-ttu-id="d8a18-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8a18-142">RELATED LINKS</span></span>

[<span data-ttu-id="d8a18-143">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d8a18-143">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="d8a18-144">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d8a18-144">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="d8a18-145">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d8a18-145">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
