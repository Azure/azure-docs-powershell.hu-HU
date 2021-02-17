---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 5e536d3174a9a71cf4f648172f3d06e6fc5ae79f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400999"
---
# <span data-ttu-id="1d4d7-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="1d4d7-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="1d4d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d4d7-102">SYNOPSIS</span></span>
<span data-ttu-id="1d4d7-103">API-változat API-kiadását hozza létre</span><span class="sxs-lookup"><span data-stu-id="1d4d7-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="1d4d7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d4d7-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d4d7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d4d7-105">DESCRIPTION</span></span>

<span data-ttu-id="1d4d7-106">A **New-AzApiManagementApiRelease** parancsmag létrehoz egy API-kiadást egy API-változathoz AZ API-kezelés környezetben.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="1d4d7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d4d7-107">EXAMPLES</span></span>

### <span data-ttu-id="1d4d7-108">1. példa: API-kiadás létrehozása API-változathoz</span><span class="sxs-lookup"><span data-stu-id="1d4d7-108">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="1d4d7-109">Ez a parancs létrehozza a `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="1d4d7-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="1d4d7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d4d7-110">PARAMETERS</span></span>

### <span data-ttu-id="1d4d7-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1d4d7-111">-ApiId</span></span>
<span data-ttu-id="1d4d7-112">Az új API azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="1d4d7-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="1d4d7-113">-ApiRevision</span></span>
<span data-ttu-id="1d4d7-114">Az Api-változat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="1d4d7-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1d4d7-115">-Context</span></span>
<span data-ttu-id="1d4d7-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1d4d7-117">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-117">This parameter is required.</span></span>

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

### <span data-ttu-id="1d4d7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d4d7-118">-DefaultProfile</span></span>
<span data-ttu-id="1d4d7-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d4d7-120">-Note</span><span class="sxs-lookup"><span data-stu-id="1d4d7-120">-Note</span></span>
<span data-ttu-id="1d4d7-121">Api kibocsátási megjegyzései.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-121">Api Release Notes.</span></span> <span data-ttu-id="1d4d7-122">Ez a paraméter nem kötelező</span><span class="sxs-lookup"><span data-stu-id="1d4d7-122">This parameter is optional</span></span>

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

### <span data-ttu-id="1d4d7-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="1d4d7-123">-ReleaseId</span></span>
<span data-ttu-id="1d4d7-124">Az Api-kiadás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="1d4d7-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-125">This parameter is optional.</span></span>
<span data-ttu-id="1d4d7-126">Ha nincs megadva azonosító, a rendszer létrehoz egy azonosítót.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="1d4d7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d4d7-127">-Confirm</span></span>
<span data-ttu-id="1d4d7-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d4d7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d4d7-129">-WhatIf</span></span>
<span data-ttu-id="1d4d7-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d4d7-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d4d7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d4d7-132">CommonParameters</span></span>
<span data-ttu-id="1d4d7-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d4d7-134">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d4d7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d4d7-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d4d7-135">INPUTS</span></span>

### <span data-ttu-id="1d4d7-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1d4d7-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1d4d7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1d4d7-137">System.String</span></span>

## <span data-ttu-id="1d4d7-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d4d7-138">OUTPUTS</span></span>

### <span data-ttu-id="1d4d7-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="1d4d7-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="1d4d7-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d4d7-140">NOTES</span></span>

## <span data-ttu-id="1d4d7-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d4d7-141">RELATED LINKS</span></span>

[<span data-ttu-id="1d4d7-142">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="1d4d7-142">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="1d4d7-143">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="1d4d7-143">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="1d4d7-144">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="1d4d7-144">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)