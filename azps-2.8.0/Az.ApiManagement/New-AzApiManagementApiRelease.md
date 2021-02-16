---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 5a5d155b8c9127d330a1f53d1fe53d42d60d46a8
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406604"
---
# <span data-ttu-id="8f624-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="8f624-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="8f624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f624-102">SYNOPSIS</span></span>
<span data-ttu-id="8f624-103">API-változat API-kiadását hozza létre</span><span class="sxs-lookup"><span data-stu-id="8f624-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="8f624-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8f624-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f624-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8f624-105">DESCRIPTION</span></span>

<span data-ttu-id="8f624-106">A **New-AzApiManagementApiRelease** parancsmag létrehoz egy API-kiadást egy API-változathoz AZ API-kezelés környezetben.</span><span class="sxs-lookup"><span data-stu-id="8f624-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="8f624-107">A kiadás az Api változatának aktuális változatként való alkalmazásához használatos.</span><span class="sxs-lookup"><span data-stu-id="8f624-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="8f624-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8f624-108">EXAMPLES</span></span>

### <span data-ttu-id="8f624-109">1. példa: API-kiadás létrehozása API-változathoz</span><span class="sxs-lookup"><span data-stu-id="8f624-109">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="8f624-110">Ez a parancs létrehozza a `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="8f624-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="8f624-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f624-111">PARAMETERS</span></span>

### <span data-ttu-id="8f624-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8f624-112">-ApiId</span></span>
<span data-ttu-id="8f624-113">Az új API azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8f624-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="8f624-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="8f624-114">-ApiRevision</span></span>
<span data-ttu-id="8f624-115">Az Api-változat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8f624-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="8f624-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8f624-116">-Context</span></span>
<span data-ttu-id="8f624-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="8f624-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8f624-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8f624-118">This parameter is required.</span></span>

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

### <span data-ttu-id="8f624-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f624-119">-DefaultProfile</span></span>
<span data-ttu-id="8f624-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f624-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f624-121">-Note</span><span class="sxs-lookup"><span data-stu-id="8f624-121">-Note</span></span>
<span data-ttu-id="8f624-122">Api kibocsátási megjegyzései.</span><span class="sxs-lookup"><span data-stu-id="8f624-122">Api Release Notes.</span></span> <span data-ttu-id="8f624-123">Ez a paraméter nem kötelező</span><span class="sxs-lookup"><span data-stu-id="8f624-123">This parameter is optional</span></span>

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

### <span data-ttu-id="8f624-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="8f624-124">-ReleaseId</span></span>
<span data-ttu-id="8f624-125">Az Api-kiadás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8f624-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="8f624-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8f624-126">This parameter is optional.</span></span>
<span data-ttu-id="8f624-127">Ha nincs megadva azonosító, a rendszer létrehoz egy azonosítót.</span><span class="sxs-lookup"><span data-stu-id="8f624-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="8f624-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f624-128">-Confirm</span></span>
<span data-ttu-id="8f624-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8f624-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f624-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f624-130">-WhatIf</span></span>
<span data-ttu-id="8f624-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8f624-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f624-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f624-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f624-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f624-133">CommonParameters</span></span>
<span data-ttu-id="8f624-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f624-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f624-135">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f624-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f624-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f624-136">INPUTS</span></span>

### <span data-ttu-id="8f624-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8f624-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8f624-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8f624-138">System.String</span></span>

## <span data-ttu-id="8f624-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f624-139">OUTPUTS</span></span>

### <span data-ttu-id="8f624-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="8f624-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="8f624-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8f624-141">NOTES</span></span>

## <span data-ttu-id="8f624-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f624-142">RELATED LINKS</span></span>

[<span data-ttu-id="8f624-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="8f624-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="8f624-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="8f624-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="8f624-145">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="8f624-145">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)