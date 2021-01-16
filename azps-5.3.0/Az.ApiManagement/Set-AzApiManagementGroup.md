---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: f4e2bb2bce0dc01f99b55497ba671999c9c2ab01
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381749"
---
# <span data-ttu-id="4c6c5-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4c6c5-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="4c6c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="4c6c5-103">Konfigurál egy API-kezelési csoportot.</span><span class="sxs-lookup"><span data-stu-id="4c6c5-103">Configures an API management group.</span></span>

## <span data-ttu-id="4c6c5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4c6c5-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c6c5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4c6c5-105">DESCRIPTION</span></span>
<span data-ttu-id="4c6c5-106">A **Set-AzApiManagementGroup** parancsmag konfigurál egy API-felügyeleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="4c6c5-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="4c6c5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4c6c5-107">EXAMPLES</span></span>

### <span data-ttu-id="4c6c5-108">1. példa: Felügyeleti csoport konfigurálása</span><span class="sxs-lookup"><span data-stu-id="4c6c5-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="4c6c5-109">Ez a parancs a Group0001 nevű felügyeleti csoportot konfigurálja.</span><span class="sxs-lookup"><span data-stu-id="4c6c5-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="4c6c5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c6c5-110">PARAMETERS</span></span>

### <span data-ttu-id="4c6c5-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4c6c5-111">-Context</span></span>
<span data-ttu-id="4c6c5-112">Egy **PsApiManagementContext objektum** egy példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c6c5-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4c6c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c6c5-113">-DefaultProfile</span></span>
<span data-ttu-id="4c6c5-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c6c5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c6c5-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="4c6c5-115">-Description</span></span>
<span data-ttu-id="4c6c5-116">A felügyeleti csoport leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c6c5-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="4c6c5-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="4c6c5-117">-GroupId</span></span>
<span data-ttu-id="4c6c5-118">A felügyeleti csoport azonosítóját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4c6c5-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="4c6c5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4c6c5-119">-Name</span></span>
<span data-ttu-id="4c6c5-120">A felügyeleti csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c6c5-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="4c6c5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c6c5-121">-PassThru</span></span>
<span data-ttu-id="4c6c5-122">passthru</span><span class="sxs-lookup"><span data-stu-id="4c6c5-122">passthru</span></span>

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

### <span data-ttu-id="4c6c5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c6c5-123">-Confirm</span></span>
<span data-ttu-id="4c6c5-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4c6c5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c6c5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c6c5-125">-WhatIf</span></span>
<span data-ttu-id="4c6c5-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4c6c5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c6c5-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4c6c5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c6c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c6c5-128">CommonParameters</span></span>
<span data-ttu-id="4c6c5-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c6c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c6c5-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c6c5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c6c5-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c6c5-131">INPUTS</span></span>

### <span data-ttu-id="4c6c5-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4c6c5-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4c6c5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4c6c5-133">System.String</span></span>

### <span data-ttu-id="4c6c5-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4c6c5-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4c6c5-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c6c5-135">OUTPUTS</span></span>

### <span data-ttu-id="4c6c5-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4c6c5-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="4c6c5-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4c6c5-137">NOTES</span></span>

## <span data-ttu-id="4c6c5-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c6c5-138">RELATED LINKS</span></span>

[<span data-ttu-id="4c6c5-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4c6c5-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="4c6c5-140">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4c6c5-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="4c6c5-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4c6c5-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


