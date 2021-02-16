---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3995506c302d2993623f12fcb7e6e2b9f96fd208
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149571"
---
# <span data-ttu-id="14e71-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="14e71-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="14e71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14e71-102">SYNOPSIS</span></span>
<span data-ttu-id="14e71-103">Módosítások mentése véglegesítés létrehozásával az aktuális konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="14e71-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="14e71-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="14e71-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14e71-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="14e71-105">DESCRIPTION</span></span>
<span data-ttu-id="14e71-106">A **Save-AzApiManagementTenantGitConfiguration** parancsmag a módosításokat úgy menti, hogy létrehoz egy véglegesítést, amely tartalmazza az aktuális konfigurációs pillanatképet a tárban lévő ágba.</span><span class="sxs-lookup"><span data-stu-id="14e71-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="14e71-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="14e71-107">EXAMPLES</span></span>

### <span data-ttu-id="14e71-108">1. példa: A konfiguráció módosításainak mentése</span><span class="sxs-lookup"><span data-stu-id="14e71-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="14e71-109">Ez a parancs úgy menti a módosításokat, hogy létrehoz egy véglegesítést az aktuális konfigurációs pillanatkép alapján a tár adott ágában.</span><span class="sxs-lookup"><span data-stu-id="14e71-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="14e71-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14e71-110">PARAMETERS</span></span>

### <span data-ttu-id="14e71-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="14e71-111">-Branch</span></span>
<span data-ttu-id="14e71-112">Annak a Git-ágnak a nevét adja meg, amelyben az aktuális konfigurációs pillanatképet el kell készíteni.</span><span class="sxs-lookup"><span data-stu-id="14e71-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="14e71-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="14e71-113">-Context</span></span>
<span data-ttu-id="14e71-114">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="14e71-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="14e71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e71-115">-DefaultProfile</span></span>
<span data-ttu-id="14e71-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14e71-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14e71-117">-Force</span><span class="sxs-lookup"><span data-stu-id="14e71-117">-Force</span></span>
<span data-ttu-id="14e71-118">Ezzel a parancsmagmal akkor is véglegesítjük az aktuális konfigurációs adatbázist a Git-tárban, ha a Git-tárban újabb módosítások vannak felülírva.</span><span class="sxs-lookup"><span data-stu-id="14e71-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="14e71-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14e71-119">-PassThru</span></span>
<span data-ttu-id="14e71-120">Azt jelzi, hogy ez a parancsmag **Egy PsApiManagementOperationResult objektumot ad vissza.**</span><span class="sxs-lookup"><span data-stu-id="14e71-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="14e71-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14e71-121">-Confirm</span></span>
<span data-ttu-id="14e71-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="14e71-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14e71-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14e71-123">-WhatIf</span></span>
<span data-ttu-id="14e71-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="14e71-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14e71-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14e71-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14e71-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e71-126">CommonParameters</span></span>
<span data-ttu-id="14e71-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14e71-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e71-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14e71-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e71-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14e71-129">INPUTS</span></span>

### <span data-ttu-id="14e71-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="14e71-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="14e71-131">System.String</span><span class="sxs-lookup"><span data-stu-id="14e71-131">System.String</span></span>

### <span data-ttu-id="14e71-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="14e71-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="14e71-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14e71-133">OUTPUTS</span></span>

### <span data-ttu-id="14e71-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="14e71-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="14e71-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="14e71-135">NOTES</span></span>

## <span data-ttu-id="14e71-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14e71-136">RELATED LINKS</span></span>

[<span data-ttu-id="14e71-137">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="14e71-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


