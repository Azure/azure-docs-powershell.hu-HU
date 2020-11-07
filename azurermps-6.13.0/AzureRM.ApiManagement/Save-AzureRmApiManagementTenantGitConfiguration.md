---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/save-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 9b297771f05b35493f8a852fd6d3450d2b5e7531
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679214"
---
# <span data-ttu-id="59a50-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="59a50-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="59a50-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59a50-102">SYNOPSIS</span></span>
<span data-ttu-id="59a50-103">A módosítások mentése az aktuális konfiguráció véglegesítése paranccsal.</span><span class="sxs-lookup"><span data-stu-id="59a50-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59a50-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59a50-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59a50-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59a50-105">DESCRIPTION</span></span>
<span data-ttu-id="59a50-106">A **Save-AzureRmApiManagementTenantGitConfiguration** parancsmag olyan véglegesítési kötelezettséget hoz létre, amely az aktuális konfigurációs pillanatképet a tárházban egy ágra menti.</span><span class="sxs-lookup"><span data-stu-id="59a50-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="59a50-107">Példák</span><span class="sxs-lookup"><span data-stu-id="59a50-107">EXAMPLES</span></span>

### <span data-ttu-id="59a50-108">Példa 1: módosítások mentése a konfigurációba</span><span class="sxs-lookup"><span data-stu-id="59a50-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="59a50-109">Ez a parancs elmenti a módosításokat, ha az aktuális konfigurációs pillanatképet véglegesítéssel a tárházban megadott ágra hozza létre.</span><span class="sxs-lookup"><span data-stu-id="59a50-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="59a50-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59a50-110">PARAMETERS</span></span>

### <span data-ttu-id="59a50-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="59a50-111">-Branch</span></span>
<span data-ttu-id="59a50-112">Annak a git-elágazásnak a nevét adja meg, amelyben az aktuális konfigurációs pillanatkép véglegesítése folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="59a50-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="59a50-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="59a50-113">-Context</span></span>
<span data-ttu-id="59a50-114">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="59a50-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="59a50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a50-115">-DefaultProfile</span></span>
<span data-ttu-id="59a50-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59a50-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a50-117">-Force</span><span class="sxs-lookup"><span data-stu-id="59a50-117">-Force</span></span>
<span data-ttu-id="59a50-118">Itt adhatja meg, hogy a parancsmag az aktuális konfigurációs adatbázist a git tárházba véglegesíti, még akkor is, ha a git repository újabb, felülírt módosításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="59a50-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="59a50-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59a50-119">-PassThru</span></span>
<span data-ttu-id="59a50-120">Azt jelzi, hogy ez a parancsmag egy **PsApiManagementOperationResult** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="59a50-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="59a50-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59a50-121">-Confirm</span></span>
<span data-ttu-id="59a50-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59a50-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59a50-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59a50-123">-WhatIf</span></span>
<span data-ttu-id="59a50-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59a50-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59a50-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59a50-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59a50-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a50-126">CommonParameters</span></span>
<span data-ttu-id="59a50-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59a50-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a50-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59a50-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a50-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59a50-129">INPUTS</span></span>

### <span data-ttu-id="59a50-130">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="59a50-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="59a50-131">System. String</span><span class="sxs-lookup"><span data-stu-id="59a50-131">System.String</span></span>

### <span data-ttu-id="59a50-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="59a50-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="59a50-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59a50-133">OUTPUTS</span></span>

### <span data-ttu-id="59a50-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="59a50-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="59a50-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59a50-135">NOTES</span></span>

## <span data-ttu-id="59a50-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59a50-136">RELATED LINKS</span></span>

[<span data-ttu-id="59a50-137">Közzététel – AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="59a50-137">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)


