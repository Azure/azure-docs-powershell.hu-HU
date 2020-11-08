---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 40d5cef72a8a1f345ac7f6389bacfb75257ccab4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012262"
---
# <span data-ttu-id="ed705-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="ed705-101">Import-AzContext</span></span>

## <span data-ttu-id="ed705-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed705-102">SYNOPSIS</span></span>
<span data-ttu-id="ed705-103">Azure-hitelesítési adatok betöltése egy fájlból.</span><span class="sxs-lookup"><span data-stu-id="ed705-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="ed705-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed705-104">SYNTAX</span></span>

### <span data-ttu-id="ed705-105">ProfileFromDisk (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed705-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed705-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="ed705-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed705-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed705-107">DESCRIPTION</span></span>
<span data-ttu-id="ed705-108">A Import-AzContext parancsmag az Azure-környezet és-környezet beállításához betölti a fájlok hitelesítési adatait.</span><span class="sxs-lookup"><span data-stu-id="ed705-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="ed705-109">Az aktuális munkamenetben futtatott parancsmagok ezekkel az információkkal hitelesíthetők az Azure Resource Manager kérései között.</span><span class="sxs-lookup"><span data-stu-id="ed705-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="ed705-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ed705-110">EXAMPLES</span></span>

### <span data-ttu-id="ed705-111">1. példa: környezet importálása AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="ed705-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ed705-112">Ebben a példában egy olyan környezetet importál egy PSAzureProfile, amely át lett adva a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="ed705-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="ed705-113">2. példa: környezet importálása JSON-fájlból</span><span class="sxs-lookup"><span data-stu-id="ed705-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ed705-114">Ebben a példában egy JSON-fájl egy olyan környezetét jelöli ki, amely át lett adva a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="ed705-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="ed705-115">Ezt a JSON-fájlt a Save-AzContext hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="ed705-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="ed705-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed705-116">PARAMETERS</span></span>

### <span data-ttu-id="ed705-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="ed705-117">-AzureContext</span></span>
<span data-ttu-id="ed705-118">{{Fill AzureContext Description}}</span><span class="sxs-lookup"><span data-stu-id="ed705-118">{{Fill AzureContext Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed705-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed705-119">-DefaultProfile</span></span>
<span data-ttu-id="ed705-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ed705-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed705-121">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="ed705-121">-Path</span></span>
<span data-ttu-id="ed705-122">A Save-AzContext paranccsal mentett környezeti információk elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed705-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

```yaml
Type: System.String
Parameter Sets: ProfileFromDisk
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed705-123">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="ed705-123">-Scope</span></span>
<span data-ttu-id="ed705-124">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="ed705-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed705-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ed705-125">-Confirm</span></span>
<span data-ttu-id="ed705-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed705-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed705-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed705-127">-WhatIf</span></span>
<span data-ttu-id="ed705-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ed705-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed705-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed705-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed705-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed705-130">CommonParameters</span></span>
<span data-ttu-id="ed705-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed705-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed705-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed705-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed705-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed705-133">INPUTS</span></span>

### <span data-ttu-id="ed705-134">Microsoft. Azure. commands. Common. Authentication. models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="ed705-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="ed705-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ed705-135">System.String</span></span>

## <span data-ttu-id="ed705-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed705-136">OUTPUTS</span></span>

### <span data-ttu-id="ed705-137">Microsoft. Azure. Command. profil. models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ed705-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="ed705-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed705-138">NOTES</span></span>

## <span data-ttu-id="ed705-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed705-139">RELATED LINKS</span></span>
