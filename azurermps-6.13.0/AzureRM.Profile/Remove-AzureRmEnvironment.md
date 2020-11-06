---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: 05a4b2a475b2bd58de706ba038f2760d133b7dbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498203"
---
# <span data-ttu-id="30987-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="30987-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="30987-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30987-102">SYNOPSIS</span></span>
<span data-ttu-id="30987-103">Eltávolítja az adott Azure-példányhoz való csatlakozáshoz szükséges végpontokat és metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="30987-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30987-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30987-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30987-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="30987-105">DESCRIPTION</span></span>
<span data-ttu-id="30987-106">A Remove-AzureRmEnvironment parancsmag eltávolítja az adott Azure-példányhoz való csatlakozáshoz szükséges végpontokat és metaadat-információkat.</span><span class="sxs-lookup"><span data-stu-id="30987-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="30987-107">Példák</span><span class="sxs-lookup"><span data-stu-id="30987-107">EXAMPLES</span></span>

### <span data-ttu-id="30987-108">Példa 1: tesztkörnyezet létrehozása és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="30987-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="30987-109">Ez a példa bemutatja, hogyan hozhat létre környezetet a AzureRmEnvironment használatával, és hogy hogyan törölheti a környezetet a Remove-AzureRmEnvironment használatával.</span><span class="sxs-lookup"><span data-stu-id="30987-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="30987-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30987-110">PARAMETERS</span></span>

### <span data-ttu-id="30987-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30987-111">-DefaultProfile</span></span>
<span data-ttu-id="30987-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30987-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30987-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="30987-113">-Name</span></span>
<span data-ttu-id="30987-114">Az eltávolítandó környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="30987-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="30987-115">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="30987-115">-Scope</span></span>
<span data-ttu-id="30987-116">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="30987-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="30987-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="30987-117">-Confirm</span></span>
<span data-ttu-id="30987-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="30987-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30987-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30987-119">-WhatIf</span></span>
<span data-ttu-id="30987-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="30987-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30987-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="30987-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30987-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30987-122">CommonParameters</span></span>
<span data-ttu-id="30987-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30987-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30987-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30987-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30987-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30987-125">INPUTS</span></span>

### <span data-ttu-id="30987-126">System. String</span><span class="sxs-lookup"><span data-stu-id="30987-126">System.String</span></span>

## <span data-ttu-id="30987-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30987-127">OUTPUTS</span></span>

### <span data-ttu-id="30987-128">Microsoft. Azure. Command. profil. models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="30987-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="30987-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30987-129">NOTES</span></span>

## <span data-ttu-id="30987-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30987-130">RELATED LINKS</span></span>

[<span data-ttu-id="30987-131">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="30987-131">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="30987-132">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="30987-132">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="30987-133">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="30987-133">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

