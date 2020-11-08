---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3995506c302d2993623f12fcb7e6e2b9f96fd208
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180659"
---
# <span data-ttu-id="3bd34-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="3bd34-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="3bd34-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3bd34-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd34-103">A módosítások mentése az aktuális konfiguráció véglegesítése paranccsal.</span><span class="sxs-lookup"><span data-stu-id="3bd34-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="3bd34-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3bd34-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bd34-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3bd34-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd34-106">A **Save-AzApiManagementTenantGitConfiguration** parancsmag olyan véglegesítési kötelezettséget hoz létre, amely az aktuális konfigurációs pillanatképet a tárházban egy ágra menti.</span><span class="sxs-lookup"><span data-stu-id="3bd34-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="3bd34-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3bd34-107">EXAMPLES</span></span>

### <span data-ttu-id="3bd34-108">Példa 1: módosítások mentése a konfigurációba</span><span class="sxs-lookup"><span data-stu-id="3bd34-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="3bd34-109">Ez a parancs elmenti a módosításokat, ha az aktuális konfigurációs pillanatképet véglegesítéssel a tárházban megadott ágra hozza létre.</span><span class="sxs-lookup"><span data-stu-id="3bd34-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="3bd34-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3bd34-110">PARAMETERS</span></span>

### <span data-ttu-id="3bd34-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="3bd34-111">-Branch</span></span>
<span data-ttu-id="3bd34-112">Annak a git-elágazásnak a nevét adja meg, amelyben az aktuális konfigurációs pillanatkép véglegesítése folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="3bd34-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="3bd34-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3bd34-113">-Context</span></span>
<span data-ttu-id="3bd34-114">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3bd34-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3bd34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd34-115">-DefaultProfile</span></span>
<span data-ttu-id="3bd34-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bd34-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bd34-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3bd34-117">-Force</span></span>
<span data-ttu-id="3bd34-118">Itt adhatja meg, hogy a parancsmag az aktuális konfigurációs adatbázist a git tárházba véglegesíti, még akkor is, ha a git repository újabb, felülírt módosításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="3bd34-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="3bd34-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bd34-119">-PassThru</span></span>
<span data-ttu-id="3bd34-120">Azt jelzi, hogy ez a parancsmag egy **PsApiManagementOperationResult** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="3bd34-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="3bd34-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3bd34-121">-Confirm</span></span>
<span data-ttu-id="3bd34-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3bd34-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bd34-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd34-123">-WhatIf</span></span>
<span data-ttu-id="3bd34-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3bd34-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bd34-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3bd34-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bd34-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd34-126">CommonParameters</span></span>
<span data-ttu-id="3bd34-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3bd34-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd34-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3bd34-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd34-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bd34-129">INPUTS</span></span>

### <span data-ttu-id="3bd34-130">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3bd34-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3bd34-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3bd34-131">System.String</span></span>

### <span data-ttu-id="3bd34-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3bd34-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3bd34-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bd34-133">OUTPUTS</span></span>

### <span data-ttu-id="3bd34-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="3bd34-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="3bd34-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3bd34-135">NOTES</span></span>

## <span data-ttu-id="3bd34-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bd34-136">RELATED LINKS</span></span>

[<span data-ttu-id="3bd34-137">Közzététel – AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="3bd34-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


