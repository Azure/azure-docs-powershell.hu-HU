---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 2c7ba44358db4e6a578f9876e26a099b2242badc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185114"
---
# <span data-ttu-id="b6de2-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6de2-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="b6de2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6de2-102">SYNOPSIS</span></span>
<span data-ttu-id="b6de2-103">Eltávolítja az adott Azure-példányhoz való csatlakozáshoz szükséges végpontokat és metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="b6de2-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="b6de2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6de2-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6de2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6de2-105">DESCRIPTION</span></span>
<span data-ttu-id="b6de2-106">A Remove-AzEnvironment parancsmag eltávolítja az adott Azure-példányhoz való csatlakozáshoz szükséges végpontokat és metaadat-információkat.</span><span class="sxs-lookup"><span data-stu-id="b6de2-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="b6de2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b6de2-107">EXAMPLES</span></span>

### <span data-ttu-id="b6de2-108">Példa 1: tesztkörnyezet létrehozása és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b6de2-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="b6de2-109">Ez a példa bemutatja, hogyan hozhat létre környezetet a AzEnvironment használatával, és hogy hogyan törölheti a környezetet a Remove-AzEnvironment használatával.</span><span class="sxs-lookup"><span data-stu-id="b6de2-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="b6de2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6de2-110">PARAMETERS</span></span>

### <span data-ttu-id="b6de2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6de2-111">-DefaultProfile</span></span>
<span data-ttu-id="b6de2-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6de2-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6de2-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6de2-113">-Name</span></span>
<span data-ttu-id="b6de2-114">Az eltávolítandó környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6de2-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="b6de2-115">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="b6de2-115">-Scope</span></span>
<span data-ttu-id="b6de2-116">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="b6de2-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="b6de2-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6de2-117">-Confirm</span></span>
<span data-ttu-id="b6de2-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6de2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6de2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6de2-119">-WhatIf</span></span>
<span data-ttu-id="b6de2-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6de2-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6de2-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6de2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6de2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6de2-122">CommonParameters</span></span>
<span data-ttu-id="b6de2-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6de2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6de2-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6de2-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6de2-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6de2-125">INPUTS</span></span>

### <span data-ttu-id="b6de2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b6de2-126">System.String</span></span>

## <span data-ttu-id="b6de2-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6de2-127">OUTPUTS</span></span>

### <span data-ttu-id="b6de2-128">Microsoft. Azure. Command. profil. models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6de2-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="b6de2-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6de2-129">NOTES</span></span>

## <span data-ttu-id="b6de2-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6de2-130">RELATED LINKS</span></span>

[<span data-ttu-id="b6de2-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6de2-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="b6de2-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6de2-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="b6de2-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6de2-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

