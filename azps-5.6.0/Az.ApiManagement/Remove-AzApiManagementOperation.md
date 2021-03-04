---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 0db56d65893c9c003261c2004435c5d231c014f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938354"
---
# <span data-ttu-id="ac3ba-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ac3ba-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="ac3ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ac3ba-103">Eltávolít egy meglévő műveletet.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-103">Removes an existing operation.</span></span>

## <span data-ttu-id="ac3ba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ac3ba-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac3ba-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ac3ba-105">DESCRIPTION</span></span>
<span data-ttu-id="ac3ba-106">A **Remove-AzApiManagementOperation parancsmag** eltávolít egy meglévő műveletet.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="ac3ba-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ac3ba-107">EXAMPLES</span></span>

### <span data-ttu-id="ac3ba-108">1. példa: Meglévő API-művelet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ac3ba-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="ac3ba-109">Ez a parancs eltávolít egy meglévő API-műveletet.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="ac3ba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac3ba-110">PARAMETERS</span></span>

### <span data-ttu-id="ac3ba-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ac3ba-111">-ApiId</span></span>
<span data-ttu-id="ac3ba-112">Az API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="ac3ba-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="ac3ba-113">-ApiRevision</span></span>
<span data-ttu-id="ac3ba-114">Az API-változat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-114">Identifier of API Revision.</span></span> <span data-ttu-id="ac3ba-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-115">This parameter is optional.</span></span> <span data-ttu-id="ac3ba-116">Ha nincs megadva, a művelet törlődik az aktuálisan aktív API-változatból.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="ac3ba-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ac3ba-117">-Context</span></span>
<span data-ttu-id="ac3ba-118">A **PsApiManagementContext egy példányát adja meg.**</span><span class="sxs-lookup"><span data-stu-id="ac3ba-118">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac3ba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac3ba-119">-DefaultProfile</span></span>
<span data-ttu-id="ac3ba-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac3ba-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ac3ba-121">-OperationId</span></span>
<span data-ttu-id="ac3ba-122">Az API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="ac3ba-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac3ba-123">-PassThru</span></span>
<span data-ttu-id="ac3ba-124">Azt jelzi, hogy ez a parancsmag $True, ha sikeres, vagy ha nem, $False értéket.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="ac3ba-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac3ba-125">-Confirm</span></span>
<span data-ttu-id="ac3ba-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac3ba-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac3ba-127">-WhatIf</span></span>
<span data-ttu-id="ac3ba-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac3ba-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac3ba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac3ba-130">CommonParameters</span></span>
<span data-ttu-id="ac3ba-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac3ba-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac3ba-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac3ba-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac3ba-133">INPUTS</span></span>

### <span data-ttu-id="ac3ba-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ac3ba-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ac3ba-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ac3ba-135">System.String</span></span>

### <span data-ttu-id="ac3ba-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ac3ba-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ac3ba-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac3ba-137">OUTPUTS</span></span>

### <span data-ttu-id="ac3ba-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac3ba-138">System.Boolean</span></span>

## <span data-ttu-id="ac3ba-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ac3ba-139">NOTES</span></span>

## <span data-ttu-id="ac3ba-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac3ba-140">RELATED LINKS</span></span>

[<span data-ttu-id="ac3ba-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ac3ba-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="ac3ba-142">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ac3ba-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="ac3ba-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ac3ba-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


