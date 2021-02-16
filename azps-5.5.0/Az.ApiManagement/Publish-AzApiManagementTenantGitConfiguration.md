---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 288bb02ffad3669615df3535aec7f691162daa2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149595"
---
# <span data-ttu-id="cfac2-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfac2-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="cfac2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfac2-102">SYNOPSIS</span></span>
<span data-ttu-id="cfac2-103">Módosításokat tesz közzé egy Git-ágból a konfigurációs adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="cfac2-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="cfac2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cfac2-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cfac2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cfac2-105">DESCRIPTION</span></span>
<span data-ttu-id="cfac2-106">A **Publish-AzApiManagementTenantGitConfiguration parancsmag** közzéteszi a módosításokat egy Git-ágból a konfigurációs adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="cfac2-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="cfac2-107">A Git-ágak módosításait közzététel nélkül is érvényesítheti.</span><span class="sxs-lookup"><span data-stu-id="cfac2-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="cfac2-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cfac2-108">EXAMPLES</span></span>

### <span data-ttu-id="cfac2-109">1. példa: Git-módosítások telepítése</span><span class="sxs-lookup"><span data-stu-id="cfac2-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="cfac2-110">Ez a parancs közzéteszi a módosításokat a megadott ágból a konfigurációs adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="cfac2-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="cfac2-111">2. példa: Git-módosítások ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="cfac2-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="cfac2-112">Ez a parancs ellenőrzi a Git-ág módosításait a konfigurációs adatbázissal szemben.</span><span class="sxs-lookup"><span data-stu-id="cfac2-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="cfac2-113">Nem tesz közzé módosításokat.</span><span class="sxs-lookup"><span data-stu-id="cfac2-113">It does not publish changes.</span></span>

## <span data-ttu-id="cfac2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfac2-114">PARAMETERS</span></span>

### <span data-ttu-id="cfac2-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="cfac2-115">-Branch</span></span>
<span data-ttu-id="cfac2-116">Annak a Git-ágnak a nevét adja meg, amelyből ez a parancsmag telepíti a konfigurációt a konfigurációs adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="cfac2-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="cfac2-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="cfac2-117">-Context</span></span>
<span data-ttu-id="cfac2-118">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="cfac2-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfac2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfac2-119">-DefaultProfile</span></span>
<span data-ttu-id="cfac2-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cfac2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfac2-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cfac2-121">-Force</span></span>
<span data-ttu-id="cfac2-122">Azt jelzi, hogy ez a parancsmag törli a frissítésben törölt termékek előfizetését.</span><span class="sxs-lookup"><span data-stu-id="cfac2-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="cfac2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfac2-123">-PassThru</span></span>
<span data-ttu-id="cfac2-124">Azt jelzi, hogy ez a parancsmag **Egy PsApiManagementOperationResult objektumot ad vissza.**</span><span class="sxs-lookup"><span data-stu-id="cfac2-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="cfac2-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="cfac2-125">-ValidateOnly</span></span>
<span data-ttu-id="cfac2-126">Azt jelzi, hogy ez a parancsmag ellenőrzi a módosításokat a megadott Git-ágban.</span><span class="sxs-lookup"><span data-stu-id="cfac2-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="cfac2-127">Nem teszi közzé a konfigurációs adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="cfac2-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="cfac2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfac2-128">-Confirm</span></span>
<span data-ttu-id="cfac2-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cfac2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfac2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfac2-130">-WhatIf</span></span>
<span data-ttu-id="cfac2-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cfac2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfac2-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cfac2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfac2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfac2-133">CommonParameters</span></span>
<span data-ttu-id="cfac2-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfac2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfac2-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cfac2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfac2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cfac2-136">INPUTS</span></span>

### <span data-ttu-id="cfac2-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cfac2-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cfac2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cfac2-138">System.String</span></span>

### <span data-ttu-id="cfac2-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cfac2-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cfac2-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfac2-140">OUTPUTS</span></span>

### <span data-ttu-id="cfac2-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="cfac2-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="cfac2-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cfac2-142">NOTES</span></span>

## <span data-ttu-id="cfac2-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfac2-143">RELATED LINKS</span></span>

[<span data-ttu-id="cfac2-144">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfac2-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


