---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: 7bdf37996fb5d407d3961ddacee4701acce2baaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919082"
---
# <span data-ttu-id="21c72-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="21c72-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="21c72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21c72-102">SYNOPSIS</span></span>
<span data-ttu-id="21c72-103">Eltávolít egy API management logger.</span><span class="sxs-lookup"><span data-stu-id="21c72-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="21c72-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="21c72-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21c72-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="21c72-105">DESCRIPTION</span></span>
<span data-ttu-id="21c72-106">A **Remove-AzApiManagementLogger** parancsmag eltávolítja az Azure API Management **Logger eszközét.**</span><span class="sxs-lookup"><span data-stu-id="21c72-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="21c72-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="21c72-107">EXAMPLES</span></span>

### <span data-ttu-id="21c72-108">1. példa: Naplózó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="21c72-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="21c72-109">Ez a parancs eltávolítja az azonosítónaplót123 azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="21c72-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="21c72-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21c72-110">PARAMETERS</span></span>

### <span data-ttu-id="21c72-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="21c72-111">-Context</span></span>
<span data-ttu-id="21c72-112">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="21c72-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="21c72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c72-113">-DefaultProfile</span></span>
<span data-ttu-id="21c72-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21c72-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21c72-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="21c72-115">-LoggerId</span></span>
<span data-ttu-id="21c72-116">Az eltávolítható naplóazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="21c72-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="21c72-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21c72-117">-PassThru</span></span>
<span data-ttu-id="21c72-118">Azt jelzi, hogy ez a parancsmag visszatérési értéke $True, ha a művelet sikeres, $False egyéb esetben.</span><span class="sxs-lookup"><span data-stu-id="21c72-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="21c72-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21c72-119">-Confirm</span></span>
<span data-ttu-id="21c72-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="21c72-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21c72-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21c72-121">-WhatIf</span></span>
<span data-ttu-id="21c72-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="21c72-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21c72-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21c72-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21c72-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c72-124">CommonParameters</span></span>
<span data-ttu-id="21c72-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21c72-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c72-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21c72-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c72-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21c72-127">INPUTS</span></span>

### <span data-ttu-id="21c72-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="21c72-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="21c72-129">System.String</span><span class="sxs-lookup"><span data-stu-id="21c72-129">System.String</span></span>

### <span data-ttu-id="21c72-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="21c72-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="21c72-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21c72-131">OUTPUTS</span></span>

### <span data-ttu-id="21c72-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="21c72-132">System.Boolean</span></span>

## <span data-ttu-id="21c72-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="21c72-133">NOTES</span></span>

## <span data-ttu-id="21c72-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21c72-134">RELATED LINKS</span></span>

[<span data-ttu-id="21c72-135">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="21c72-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="21c72-136">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="21c72-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="21c72-137">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="21c72-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


