---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/save-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 7401c359a9af82d1b65749a3276aada89ab9320d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492409"
---
# <span data-ttu-id="7bea2-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bea2-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="7bea2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7bea2-102">SYNOPSIS</span></span>
<span data-ttu-id="7bea2-103">A módosítások mentése az aktuális konfiguráció véglegesítése paranccsal.</span><span class="sxs-lookup"><span data-stu-id="7bea2-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bea2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7bea2-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bea2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7bea2-105">DESCRIPTION</span></span>
<span data-ttu-id="7bea2-106">A **Save-AzureRmApiManagementTenantGitConfiguration** parancsmag olyan véglegesítési kötelezettséget hoz létre, amely az aktuális konfigurációs pillanatképet a tárházban egy ágra menti.</span><span class="sxs-lookup"><span data-stu-id="7bea2-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="7bea2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7bea2-107">EXAMPLES</span></span>

### <span data-ttu-id="7bea2-108">Példa 1: módosítások mentése a konfigurációba</span><span class="sxs-lookup"><span data-stu-id="7bea2-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="7bea2-109">Ez a parancs elmenti a módosításokat, ha az aktuális konfigurációs pillanatképet véglegesítéssel a tárházban megadott ágra hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7bea2-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="7bea2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7bea2-110">PARAMETERS</span></span>

### <span data-ttu-id="7bea2-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="7bea2-111">-Branch</span></span>
<span data-ttu-id="7bea2-112">Annak a git-elágazásnak a nevét adja meg, amelyben az aktuális konfigurációs pillanatkép véglegesítése folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="7bea2-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bea2-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7bea2-113">-Context</span></span>
<span data-ttu-id="7bea2-114">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7bea2-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bea2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bea2-115">-DefaultProfile</span></span>
<span data-ttu-id="7bea2-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7bea2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bea2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7bea2-117">-Force</span></span>
<span data-ttu-id="7bea2-118">Itt adhatja meg, hogy a parancsmag az aktuális konfigurációs adatbázist a git tárházba véglegesíti, még akkor is, ha a git repository újabb, felülírt módosításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="7bea2-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bea2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bea2-119">-PassThru</span></span>
<span data-ttu-id="7bea2-120">Azt jelzi, hogy ez a parancsmag egy **PsApiManagementOperationResult** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="7bea2-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bea2-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7bea2-121">-Confirm</span></span>
<span data-ttu-id="7bea2-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7bea2-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bea2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bea2-123">-WhatIf</span></span>
<span data-ttu-id="7bea2-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7bea2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bea2-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7bea2-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bea2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bea2-126">CommonParameters</span></span>
<span data-ttu-id="7bea2-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7bea2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bea2-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bea2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bea2-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bea2-129">INPUTS</span></span>

### <span data-ttu-id="7bea2-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="7bea2-130">None</span></span>
<span data-ttu-id="7bea2-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7bea2-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7bea2-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bea2-132">OUTPUTS</span></span>

### <span data-ttu-id="7bea2-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="7bea2-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="7bea2-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7bea2-134">NOTES</span></span>

## <span data-ttu-id="7bea2-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7bea2-135">RELATED LINKS</span></span>

[<span data-ttu-id="7bea2-136">Közzététel – AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bea2-136">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)


