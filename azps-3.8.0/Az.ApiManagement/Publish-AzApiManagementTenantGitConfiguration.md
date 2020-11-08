---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 288bb02ffad3669615df3535aec7f691162daa2a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012204"
---
# <span data-ttu-id="393ce-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="393ce-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="393ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="393ce-102">SYNOPSIS</span></span>
<span data-ttu-id="393ce-103">Egy git ág változásait a konfigurációs adatbázisba teszi közzé.</span><span class="sxs-lookup"><span data-stu-id="393ce-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="393ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="393ce-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="393ce-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="393ce-105">DESCRIPTION</span></span>
<span data-ttu-id="393ce-106">A **Közzététel – AzApiManagementTenantGitConfiguration** parancsmag egy git ág módosításait a konfigurációs adatbázisba teszi közzé.</span><span class="sxs-lookup"><span data-stu-id="393ce-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="393ce-107">Másik lehetőségként az is ellenőrizhető, hogy egy git ág módosításai közzététel nélkül is ellenőrizhetők.</span><span class="sxs-lookup"><span data-stu-id="393ce-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="393ce-108">Példák</span><span class="sxs-lookup"><span data-stu-id="393ce-108">EXAMPLES</span></span>

### <span data-ttu-id="393ce-109">1. példa: a git-módosítások telepítése</span><span class="sxs-lookup"><span data-stu-id="393ce-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="393ce-110">Ez a parancs közzéteszi a megadott ágra vonatkozó módosításokat a konfigurációs adatbázissal.</span><span class="sxs-lookup"><span data-stu-id="393ce-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="393ce-111">2. példa: a git-módosítások érvényesítése</span><span class="sxs-lookup"><span data-stu-id="393ce-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="393ce-112">Ez a parancs ellenőrzi a git ág változásait a konfigurációs adatbázissal.</span><span class="sxs-lookup"><span data-stu-id="393ce-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="393ce-113">Nem teszi közzé a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="393ce-113">It does not publish changes.</span></span>

## <span data-ttu-id="393ce-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="393ce-114">PARAMETERS</span></span>

### <span data-ttu-id="393ce-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="393ce-115">-Branch</span></span>
<span data-ttu-id="393ce-116">Annak a git-elágazásnak a nevét adja meg, amelyből ez a parancsmag telepíti a konfigurációt a konfigurációs adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="393ce-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="393ce-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="393ce-117">-Context</span></span>
<span data-ttu-id="393ce-118">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="393ce-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="393ce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="393ce-119">-DefaultProfile</span></span>
<span data-ttu-id="393ce-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="393ce-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="393ce-121">-Force</span><span class="sxs-lookup"><span data-stu-id="393ce-121">-Force</span></span>
<span data-ttu-id="393ce-122">Azt jelzi, hogy ez a parancsmag törli a frissítésben törölt termékek előfizetéseit.</span><span class="sxs-lookup"><span data-stu-id="393ce-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="393ce-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="393ce-123">-PassThru</span></span>
<span data-ttu-id="393ce-124">Azt jelzi, hogy ez a parancsmag egy **PsApiManagementOperationResult** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="393ce-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="393ce-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="393ce-125">-ValidateOnly</span></span>
<span data-ttu-id="393ce-126">Jelzi, hogy ez a parancsmag ellenőrzi a megadott git-ág módosításait.</span><span class="sxs-lookup"><span data-stu-id="393ce-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="393ce-127">A beállítási adatbázis nem tesz közzé.</span><span class="sxs-lookup"><span data-stu-id="393ce-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="393ce-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="393ce-128">-Confirm</span></span>
<span data-ttu-id="393ce-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="393ce-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="393ce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="393ce-130">-WhatIf</span></span>
<span data-ttu-id="393ce-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="393ce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="393ce-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="393ce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="393ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393ce-133">CommonParameters</span></span>
<span data-ttu-id="393ce-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="393ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393ce-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="393ce-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393ce-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="393ce-136">INPUTS</span></span>

### <span data-ttu-id="393ce-137">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="393ce-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="393ce-138">System. String</span><span class="sxs-lookup"><span data-stu-id="393ce-138">System.String</span></span>

### <span data-ttu-id="393ce-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="393ce-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="393ce-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="393ce-140">OUTPUTS</span></span>

### <span data-ttu-id="393ce-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="393ce-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="393ce-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="393ce-142">NOTES</span></span>

## <span data-ttu-id="393ce-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="393ce-143">RELATED LINKS</span></span>

[<span data-ttu-id="393ce-144">Mentés-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="393ce-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


