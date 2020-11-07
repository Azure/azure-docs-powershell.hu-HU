---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: f816488e6334c0e9c410bb1c24f46501a1fefe85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665647"
---
# <span data-ttu-id="97a50-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="97a50-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="97a50-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97a50-102">SYNOPSIS</span></span>
<span data-ttu-id="97a50-103">API-kiadás API-változatának létrehozása</span><span class="sxs-lookup"><span data-stu-id="97a50-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="97a50-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97a50-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97a50-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97a50-105">DESCRIPTION</span></span>

<span data-ttu-id="97a50-106">A **New-AzApiManagementApiRelease** parancsmag API-kiadást hoz létre az API-kezelési környezet API-verziójában.</span><span class="sxs-lookup"><span data-stu-id="97a50-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="97a50-107">Példák</span><span class="sxs-lookup"><span data-stu-id="97a50-107">EXAMPLES</span></span>

### <span data-ttu-id="97a50-108">1. példa: API-kiadás létrehozása API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="97a50-108">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


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

<span data-ttu-id="97a50-109">Ez a parancs API-kiadást hoz létre `2` a módosítások számára `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="97a50-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="97a50-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97a50-110">PARAMETERS</span></span>

### <span data-ttu-id="97a50-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="97a50-111">-ApiId</span></span>
<span data-ttu-id="97a50-112">Azonosítót az új API-hoz.</span><span class="sxs-lookup"><span data-stu-id="97a50-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="97a50-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="97a50-113">-ApiRevision</span></span>
<span data-ttu-id="97a50-114">Az API-módosítás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="97a50-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="97a50-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="97a50-115">-Context</span></span>
<span data-ttu-id="97a50-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="97a50-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="97a50-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="97a50-117">This parameter is required.</span></span>

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

### <span data-ttu-id="97a50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a50-118">-DefaultProfile</span></span>
<span data-ttu-id="97a50-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97a50-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97a50-120">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="97a50-120">-Note</span></span>
<span data-ttu-id="97a50-121">API-kibocsátási megjegyzések.</span><span class="sxs-lookup"><span data-stu-id="97a50-121">Api Release Notes.</span></span> <span data-ttu-id="97a50-122">Ez a paraméter nem kötelező</span><span class="sxs-lookup"><span data-stu-id="97a50-122">This parameter is optional</span></span>

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

### <span data-ttu-id="97a50-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="97a50-123">-ReleaseId</span></span>
<span data-ttu-id="97a50-124">Az API-kiadás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="97a50-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="97a50-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="97a50-125">This parameter is optional.</span></span>
<span data-ttu-id="97a50-126">Ha a program nem hoz létre megadott azonosítót.</span><span class="sxs-lookup"><span data-stu-id="97a50-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="97a50-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="97a50-127">-Confirm</span></span>
<span data-ttu-id="97a50-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="97a50-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97a50-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97a50-129">-WhatIf</span></span>
<span data-ttu-id="97a50-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="97a50-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97a50-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97a50-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97a50-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a50-132">CommonParameters</span></span>
<span data-ttu-id="97a50-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97a50-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a50-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97a50-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a50-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97a50-135">INPUTS</span></span>

### <span data-ttu-id="97a50-136">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="97a50-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="97a50-137">System. String</span><span class="sxs-lookup"><span data-stu-id="97a50-137">System.String</span></span>

## <span data-ttu-id="97a50-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97a50-138">OUTPUTS</span></span>

### <span data-ttu-id="97a50-139">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="97a50-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="97a50-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97a50-140">NOTES</span></span>

## <span data-ttu-id="97a50-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97a50-141">RELATED LINKS</span></span>

[<span data-ttu-id="97a50-142">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="97a50-142">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="97a50-143">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="97a50-143">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="97a50-144">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="97a50-144">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)