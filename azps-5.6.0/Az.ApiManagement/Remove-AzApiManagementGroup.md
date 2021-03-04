---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 4ddeee0b0efbb55d98e8e14be1bc84ea83b38e6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924274"
---
# <span data-ttu-id="93e18-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="93e18-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="93e18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93e18-102">SYNOPSIS</span></span>
<span data-ttu-id="93e18-103">Eltávolít egy meglévő API-felügyeleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="93e18-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="93e18-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="93e18-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93e18-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="93e18-105">DESCRIPTION</span></span>
<span data-ttu-id="93e18-106">A **Remove-AzApiManagementGroup** parancsmag eltávolít egy meglévő API-felügyeleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="93e18-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="93e18-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="93e18-107">EXAMPLES</span></span>

### <span data-ttu-id="93e18-108">1. példa: Meglévő felügyeleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="93e18-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="93e18-109">Ez a parancs eltávolít egy Group0001 nevű meglévő felügyeleti csoportot, és nem kér megerősítést a felhasználótól.</span><span class="sxs-lookup"><span data-stu-id="93e18-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="93e18-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93e18-110">PARAMETERS</span></span>

### <span data-ttu-id="93e18-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="93e18-111">-Context</span></span>
<span data-ttu-id="93e18-112">Egy **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="93e18-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="93e18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e18-113">-DefaultProfile</span></span>
<span data-ttu-id="93e18-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93e18-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93e18-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="93e18-115">-GroupId</span></span>
<span data-ttu-id="93e18-116">Egy felügyeleti csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="93e18-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="93e18-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93e18-117">-PassThru</span></span>
<span data-ttu-id="93e18-118">Azt jelzi, hogy ez a parancsmag $True, ha sikeres, vagy ha nem, $False értéket.</span><span class="sxs-lookup"><span data-stu-id="93e18-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="93e18-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93e18-119">-Confirm</span></span>
<span data-ttu-id="93e18-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="93e18-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e18-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e18-121">-WhatIf</span></span>
<span data-ttu-id="93e18-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="93e18-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93e18-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93e18-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e18-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e18-124">CommonParameters</span></span>
<span data-ttu-id="93e18-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93e18-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e18-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93e18-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e18-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93e18-127">INPUTS</span></span>

### <span data-ttu-id="93e18-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="93e18-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="93e18-129">System.String</span><span class="sxs-lookup"><span data-stu-id="93e18-129">System.String</span></span>

### <span data-ttu-id="93e18-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="93e18-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="93e18-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93e18-131">OUTPUTS</span></span>

### <span data-ttu-id="93e18-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93e18-132">System.Boolean</span></span>

## <span data-ttu-id="93e18-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="93e18-133">NOTES</span></span>

## <span data-ttu-id="93e18-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93e18-134">RELATED LINKS</span></span>

[<span data-ttu-id="93e18-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="93e18-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="93e18-136">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="93e18-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="93e18-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="93e18-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


