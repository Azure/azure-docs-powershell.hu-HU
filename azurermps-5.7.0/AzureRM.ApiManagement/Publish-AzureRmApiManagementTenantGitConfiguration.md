---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/publish-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3879def437171e9de2cad6f328ef6bf15bed3d48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495483"
---
# <span data-ttu-id="fd6c8-101">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd6c8-101">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="fd6c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd6c8-102">SYNOPSIS</span></span>
<span data-ttu-id="fd6c8-103">Egy git ág változásait a konfigurációs adatbázisba teszi közzé.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-103">Publishes changes from a Git branch to the configuration database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd6c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd6c8-104">SYNTAX</span></span>

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd6c8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd6c8-105">DESCRIPTION</span></span>
<span data-ttu-id="fd6c8-106">A **Közzététel – AzureRmApiManagementTenantGitConfiguration** parancsmag egy git ág módosításait a konfigurációs adatbázisba teszi közzé.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-106">The **Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="fd6c8-107">Másik lehetőségként az is ellenőrizhető, hogy egy git ág módosításai közzététel nélkül is ellenőrizhetők.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="fd6c8-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fd6c8-108">EXAMPLES</span></span>

### <span data-ttu-id="fd6c8-109">1. példa: a git-módosítások telepítése</span><span class="sxs-lookup"><span data-stu-id="fd6c8-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="fd6c8-110">Ez a parancs közzéteszi a megadott ágra vonatkozó módosításokat a konfigurációs adatbázissal.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="fd6c8-111">2. példa: a git-módosítások érvényesítése</span><span class="sxs-lookup"><span data-stu-id="fd6c8-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="fd6c8-112">Ez a parancs ellenőrzi a git ág változásait a konfigurációs adatbázissal.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="fd6c8-113">Nem teszi közzé a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-113">It does not publish changes.</span></span>

## <span data-ttu-id="fd6c8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd6c8-114">PARAMETERS</span></span>

### <span data-ttu-id="fd6c8-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="fd6c8-115">-Branch</span></span>
<span data-ttu-id="fd6c8-116">Annak a git-elágazásnak a nevét adja meg, amelyből ez a parancsmag telepíti a konfigurációt a konfigurációs adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="fd6c8-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fd6c8-117">-Context</span></span>
<span data-ttu-id="fd6c8-118">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fd6c8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd6c8-119">-DefaultProfile</span></span>
<span data-ttu-id="fd6c8-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="fd6c8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fd6c8-121">-Force</span></span>
<span data-ttu-id="fd6c8-122">Azt jelzi, hogy ez a parancsmag törli a frissítésben törölt termékek előfizetéseit.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="fd6c8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd6c8-123">-PassThru</span></span>
<span data-ttu-id="fd6c8-124">Azt jelzi, hogy ez a parancsmag egy **PsApiManagementOperationResult** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="fd6c8-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="fd6c8-125">-ValidateOnly</span></span>
<span data-ttu-id="fd6c8-126">Jelzi, hogy ez a parancsmag ellenőrzi a megadott git-ág módosításait.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="fd6c8-127">A beállítási adatbázis nem tesz közzé.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="fd6c8-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd6c8-128">-Confirm</span></span>
<span data-ttu-id="fd6c8-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd6c8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd6c8-130">-WhatIf</span></span>
<span data-ttu-id="fd6c8-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd6c8-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd6c8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd6c8-133">CommonParameters</span></span>
<span data-ttu-id="fd6c8-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd6c8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd6c8-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd6c8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd6c8-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd6c8-136">INPUTS</span></span>

### <span data-ttu-id="fd6c8-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="fd6c8-137">None</span></span>
<span data-ttu-id="fd6c8-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fd6c8-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd6c8-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd6c8-139">OUTPUTS</span></span>

### <span data-ttu-id="fd6c8-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="fd6c8-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="fd6c8-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd6c8-141">NOTES</span></span>

## <span data-ttu-id="fd6c8-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd6c8-142">RELATED LINKS</span></span>

[<span data-ttu-id="fd6c8-143">Mentés-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd6c8-143">Save-AzureRmApiManagementTenantGitConfiguration</span></span>](./Save-AzureRmApiManagementTenantGitConfiguration.md)


