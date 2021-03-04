---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: c243cd47300d2b361e37766ab7e2e5bc906cb2ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925322"
---
# <span data-ttu-id="13079-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="13079-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="13079-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13079-102">SYNOPSIS</span></span>
<span data-ttu-id="13079-103">Konfigurál egy API-kezelési csoportot.</span><span class="sxs-lookup"><span data-stu-id="13079-103">Configures an API management group.</span></span>

## <span data-ttu-id="13079-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13079-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13079-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13079-105">DESCRIPTION</span></span>
<span data-ttu-id="13079-106">A **Set-AzApiManagementGroup** parancsmag konfigurál egy API-felügyeleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="13079-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="13079-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13079-107">EXAMPLES</span></span>

### <span data-ttu-id="13079-108">1. példa: Felügyeleti csoport konfigurálása</span><span class="sxs-lookup"><span data-stu-id="13079-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="13079-109">Ez a parancs a Group0001 nevű felügyeleti csoportot konfigurálja.</span><span class="sxs-lookup"><span data-stu-id="13079-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="13079-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13079-110">PARAMETERS</span></span>

### <span data-ttu-id="13079-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="13079-111">-Context</span></span>
<span data-ttu-id="13079-112">Egy **PsApiManagementContext objektum** egy példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="13079-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="13079-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13079-113">-DefaultProfile</span></span>
<span data-ttu-id="13079-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13079-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13079-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="13079-115">-Description</span></span>
<span data-ttu-id="13079-116">A felügyeleti csoport leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="13079-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="13079-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="13079-117">-GroupId</span></span>
<span data-ttu-id="13079-118">A felügyeleti csoport azonosítóját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="13079-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="13079-119">-Name</span><span class="sxs-lookup"><span data-stu-id="13079-119">-Name</span></span>
<span data-ttu-id="13079-120">A felügyeleti csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13079-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="13079-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13079-121">-PassThru</span></span>
<span data-ttu-id="13079-122">passthru</span><span class="sxs-lookup"><span data-stu-id="13079-122">passthru</span></span>

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

### <span data-ttu-id="13079-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13079-123">-Confirm</span></span>
<span data-ttu-id="13079-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="13079-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13079-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13079-125">-WhatIf</span></span>
<span data-ttu-id="13079-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="13079-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13079-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13079-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13079-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13079-128">CommonParameters</span></span>
<span data-ttu-id="13079-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13079-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13079-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13079-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13079-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13079-131">INPUTS</span></span>

### <span data-ttu-id="13079-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="13079-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="13079-133">System.String</span><span class="sxs-lookup"><span data-stu-id="13079-133">System.String</span></span>

### <span data-ttu-id="13079-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="13079-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="13079-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13079-135">OUTPUTS</span></span>

### <span data-ttu-id="13079-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="13079-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="13079-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13079-137">NOTES</span></span>

## <span data-ttu-id="13079-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13079-138">RELATED LINKS</span></span>

[<span data-ttu-id="13079-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="13079-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="13079-140">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="13079-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="13079-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="13079-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


