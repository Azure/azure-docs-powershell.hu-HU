---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: f4e2bb2bce0dc01f99b55497ba671999c9c2ab01
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365776"
---
# <span data-ttu-id="e99e1-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e99e1-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="e99e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e99e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e99e1-103">Konfigurál egy API-kezelési csoportot.</span><span class="sxs-lookup"><span data-stu-id="e99e1-103">Configures an API management group.</span></span>

## <span data-ttu-id="e99e1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e99e1-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e99e1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e99e1-105">DESCRIPTION</span></span>
<span data-ttu-id="e99e1-106">A **Set-AzApiManagementGroup** parancsmag konfigurál egy API-felügyeleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="e99e1-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="e99e1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e99e1-107">EXAMPLES</span></span>

### <span data-ttu-id="e99e1-108">1. példa: Felügyeleti csoport konfigurálása</span><span class="sxs-lookup"><span data-stu-id="e99e1-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="e99e1-109">Ez a parancs a Group0001 nevű felügyeleti csoportot konfigurálja.</span><span class="sxs-lookup"><span data-stu-id="e99e1-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="e99e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e99e1-110">PARAMETERS</span></span>

### <span data-ttu-id="e99e1-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e99e1-111">-Context</span></span>
<span data-ttu-id="e99e1-112">Egy **PsApiManagementContext objektum** egy példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e99e1-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e99e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e99e1-113">-DefaultProfile</span></span>
<span data-ttu-id="e99e1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e99e1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e99e1-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e99e1-115">-Description</span></span>
<span data-ttu-id="e99e1-116">A felügyeleti csoport leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="e99e1-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="e99e1-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="e99e1-117">-GroupId</span></span>
<span data-ttu-id="e99e1-118">A felügyeleti csoport azonosítóját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="e99e1-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="e99e1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e99e1-119">-Name</span></span>
<span data-ttu-id="e99e1-120">A felügyeleti csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e99e1-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="e99e1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e99e1-121">-PassThru</span></span>
<span data-ttu-id="e99e1-122">passthru</span><span class="sxs-lookup"><span data-stu-id="e99e1-122">passthru</span></span>

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

### <span data-ttu-id="e99e1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e99e1-123">-Confirm</span></span>
<span data-ttu-id="e99e1-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e99e1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e99e1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e99e1-125">-WhatIf</span></span>
<span data-ttu-id="e99e1-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e99e1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e99e1-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e99e1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e99e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e99e1-128">CommonParameters</span></span>
<span data-ttu-id="e99e1-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e99e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e99e1-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e99e1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e99e1-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e99e1-131">INPUTS</span></span>

### <span data-ttu-id="e99e1-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e99e1-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e99e1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e99e1-133">System.String</span></span>

### <span data-ttu-id="e99e1-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e99e1-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e99e1-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e99e1-135">OUTPUTS</span></span>

### <span data-ttu-id="e99e1-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e99e1-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="e99e1-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e99e1-137">NOTES</span></span>

## <span data-ttu-id="e99e1-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e99e1-138">RELATED LINKS</span></span>

[<span data-ttu-id="e99e1-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e99e1-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="e99e1-140">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e99e1-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="e99e1-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e99e1-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


