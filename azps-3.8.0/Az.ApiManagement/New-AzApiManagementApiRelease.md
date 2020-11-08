---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 9b2b94fbd6a308f9d927483e78e060a273354738
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014998"
---
# <span data-ttu-id="59a04-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="59a04-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="59a04-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59a04-102">SYNOPSIS</span></span>
<span data-ttu-id="59a04-103">API-kiadás API-változatának létrehozása</span><span class="sxs-lookup"><span data-stu-id="59a04-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="59a04-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59a04-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59a04-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59a04-105">DESCRIPTION</span></span>

<span data-ttu-id="59a04-106">A **New-AzApiManagementApiRelease** parancsmag API-kiadást hoz létre az API-kezelési környezet API-verziójában.</span><span class="sxs-lookup"><span data-stu-id="59a04-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="59a04-107">A kiadás segítségével az API-t a jelenlegi Átdolgozásként végezheti el.</span><span class="sxs-lookup"><span data-stu-id="59a04-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="59a04-108">Példák</span><span class="sxs-lookup"><span data-stu-id="59a04-108">EXAMPLES</span></span>

### <span data-ttu-id="59a04-109">1. példa: API-kiadás létrehozása API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="59a04-109">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="59a04-110">Ez a parancs API-kiadást hoz létre `2` a módosítások számára `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="59a04-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="59a04-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59a04-111">PARAMETERS</span></span>

### <span data-ttu-id="59a04-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="59a04-112">-ApiId</span></span>
<span data-ttu-id="59a04-113">Azonosítót az új API-hoz.</span><span class="sxs-lookup"><span data-stu-id="59a04-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="59a04-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="59a04-114">-ApiRevision</span></span>
<span data-ttu-id="59a04-115">Az API-módosítás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="59a04-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="59a04-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="59a04-116">-Context</span></span>
<span data-ttu-id="59a04-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="59a04-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="59a04-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="59a04-118">This parameter is required.</span></span>

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

### <span data-ttu-id="59a04-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a04-119">-DefaultProfile</span></span>
<span data-ttu-id="59a04-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59a04-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59a04-121">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="59a04-121">-Note</span></span>
<span data-ttu-id="59a04-122">API-kibocsátási megjegyzések.</span><span class="sxs-lookup"><span data-stu-id="59a04-122">Api Release Notes.</span></span> <span data-ttu-id="59a04-123">Ez a paraméter nem kötelező</span><span class="sxs-lookup"><span data-stu-id="59a04-123">This parameter is optional</span></span>

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

### <span data-ttu-id="59a04-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="59a04-124">-ReleaseId</span></span>
<span data-ttu-id="59a04-125">Az API-kiadás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="59a04-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="59a04-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="59a04-126">This parameter is optional.</span></span>
<span data-ttu-id="59a04-127">Ha a program nem hoz létre megadott azonosítót.</span><span class="sxs-lookup"><span data-stu-id="59a04-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="59a04-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59a04-128">-Confirm</span></span>
<span data-ttu-id="59a04-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59a04-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59a04-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59a04-130">-WhatIf</span></span>
<span data-ttu-id="59a04-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59a04-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59a04-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59a04-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59a04-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a04-133">CommonParameters</span></span>
<span data-ttu-id="59a04-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59a04-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a04-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="59a04-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a04-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59a04-136">INPUTS</span></span>

### <span data-ttu-id="59a04-137">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="59a04-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="59a04-138">System. String</span><span class="sxs-lookup"><span data-stu-id="59a04-138">System.String</span></span>

## <span data-ttu-id="59a04-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59a04-139">OUTPUTS</span></span>

### <span data-ttu-id="59a04-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="59a04-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="59a04-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59a04-141">NOTES</span></span>

## <span data-ttu-id="59a04-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59a04-142">RELATED LINKS</span></span>

[<span data-ttu-id="59a04-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="59a04-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="59a04-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="59a04-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="59a04-145">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="59a04-145">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)