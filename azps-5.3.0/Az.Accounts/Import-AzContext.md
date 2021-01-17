---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 40d5cef72a8a1f345ac7f6389bacfb75257ccab4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469213"
---
# <span data-ttu-id="e5f45-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="e5f45-101">Import-AzContext</span></span>

## <span data-ttu-id="e5f45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5f45-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f45-103">Egy fájlból betölti az Azure-hitelesítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="e5f45-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="e5f45-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e5f45-104">SYNTAX</span></span>

### <span data-ttu-id="e5f45-105">ProfileFromDisk (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5f45-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f45-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="e5f45-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5f45-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e5f45-107">DESCRIPTION</span></span>
<span data-ttu-id="e5f45-108">A Import-AzContext parancsmag egy fájlból betölti a hitelesítési adatokat az Azure környezetének és környezetének beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="e5f45-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="e5f45-109">Az aktuális munkamenetben futtatott parancsmagok ezeket az adatokat használva hitelesítik az Azure Resource Managerhez való kérelmeket.</span><span class="sxs-lookup"><span data-stu-id="e5f45-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="e5f45-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e5f45-110">EXAMPLES</span></span>

### <span data-ttu-id="e5f45-111">1. példa: Környezet importálása AzureRmProfile-fiókból</span><span class="sxs-lookup"><span data-stu-id="e5f45-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="e5f45-112">Ez a példa egy, a parancsmagnak átadott PSAzureProfile-környezetből importálja a környezetét.</span><span class="sxs-lookup"><span data-stu-id="e5f45-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="e5f45-113">2. példa: Környezet importálása JSON-fájlból</span><span class="sxs-lookup"><span data-stu-id="e5f45-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="e5f45-114">Ez a példa kiválaszt egy környezetet egy JSON-fájlból, amely át van adhatja a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="e5f45-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="e5f45-115">Ezt a JSON-fájlt a Save-AzContext fájlból lehet létrehozni.</span><span class="sxs-lookup"><span data-stu-id="e5f45-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="e5f45-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5f45-116">PARAMETERS</span></span>

### <span data-ttu-id="e5f45-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="e5f45-117">-AzureContext</span></span>
<span data-ttu-id="e5f45-118">{{Fill AzureContext Description}}</span><span class="sxs-lookup"><span data-stu-id="e5f45-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="e5f45-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f45-119">-DefaultProfile</span></span>
<span data-ttu-id="e5f45-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e5f45-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5f45-121">-Path</span><span class="sxs-lookup"><span data-stu-id="e5f45-121">-Path</span></span>
<span data-ttu-id="e5f45-122">A Save-AzContext használatával mentett környezeti információk elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5f45-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="e5f45-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="e5f45-123">-Scope</span></span>
<span data-ttu-id="e5f45-124">Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.</span><span class="sxs-lookup"><span data-stu-id="e5f45-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="e5f45-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5f45-125">-Confirm</span></span>
<span data-ttu-id="e5f45-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e5f45-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5f45-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5f45-127">-WhatIf</span></span>
<span data-ttu-id="e5f45-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e5f45-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5f45-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5f45-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5f45-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f45-130">CommonParameters</span></span>
<span data-ttu-id="e5f45-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5f45-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f45-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5f45-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f45-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5f45-133">INPUTS</span></span>

### <span data-ttu-id="e5f45-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="e5f45-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="e5f45-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e5f45-135">System.String</span></span>

## <span data-ttu-id="e5f45-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5f45-136">OUTPUTS</span></span>

### <span data-ttu-id="e5f45-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="e5f45-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="e5f45-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e5f45-138">NOTES</span></span>

## <span data-ttu-id="e5f45-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5f45-139">RELATED LINKS</span></span>
