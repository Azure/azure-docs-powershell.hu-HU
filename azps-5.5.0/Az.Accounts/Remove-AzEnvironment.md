---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 2c7ba44358db4e6a578f9876e26a099b2242badc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157659"
---
# <span data-ttu-id="26892-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="26892-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="26892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26892-102">SYNOPSIS</span></span>
<span data-ttu-id="26892-103">Eltávolítja az adott Azure-példányhoz való csatlakozás végpontját és metaadatait.</span><span class="sxs-lookup"><span data-stu-id="26892-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="26892-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26892-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26892-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26892-105">DESCRIPTION</span></span>
<span data-ttu-id="26892-106">A Remove-AzEnvironment parancsmag eltávolítja az adott Azure-példányhoz való csatlakozás végpontját és metaadatait.</span><span class="sxs-lookup"><span data-stu-id="26892-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="26892-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26892-107">EXAMPLES</span></span>

### <span data-ttu-id="26892-108">1. példa: Tesztkörnyezet létrehozása és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="26892-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="26892-109">Az alábbi példa bemutatja, hogy miként hozhat létre egy környezetet az Add-AzEnvironment használatával, majd hogyan törölheti a környezetet a Remove-AzEnvironment használatával.</span><span class="sxs-lookup"><span data-stu-id="26892-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="26892-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26892-110">PARAMETERS</span></span>

### <span data-ttu-id="26892-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26892-111">-DefaultProfile</span></span>
<span data-ttu-id="26892-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26892-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26892-113">-Name</span><span class="sxs-lookup"><span data-stu-id="26892-113">-Name</span></span>
<span data-ttu-id="26892-114">Az eltávolítható környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26892-114">Specifies the name of the environment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26892-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="26892-115">-Scope</span></span>
<span data-ttu-id="26892-116">Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.</span><span class="sxs-lookup"><span data-stu-id="26892-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="26892-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26892-117">-Confirm</span></span>
<span data-ttu-id="26892-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="26892-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26892-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26892-119">-WhatIf</span></span>
<span data-ttu-id="26892-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="26892-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26892-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26892-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26892-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26892-122">CommonParameters</span></span>
<span data-ttu-id="26892-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26892-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26892-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26892-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26892-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26892-125">INPUTS</span></span>

### <span data-ttu-id="26892-126">System.String</span><span class="sxs-lookup"><span data-stu-id="26892-126">System.String</span></span>

## <span data-ttu-id="26892-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26892-127">OUTPUTS</span></span>

### <span data-ttu-id="26892-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="26892-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="26892-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26892-129">NOTES</span></span>

## <span data-ttu-id="26892-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26892-130">RELATED LINKS</span></span>

[<span data-ttu-id="26892-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="26892-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="26892-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="26892-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="26892-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="26892-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

