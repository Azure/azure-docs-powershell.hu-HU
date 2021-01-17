---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: c57f8a7ce6b4f7275e724c777c2e6dfd54a680ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466898"
---
# <span data-ttu-id="3d169-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d169-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="3d169-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d169-102">SYNOPSIS</span></span>
<span data-ttu-id="3d169-103">Módosítja a megadott előfizetés aktuális tárfiókját.</span><span class="sxs-lookup"><span data-stu-id="3d169-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="3d169-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3d169-104">SYNTAX</span></span>

### <span data-ttu-id="3d169-105">UsingResourceGroupAndNameParameterSet (default)</span><span class="sxs-lookup"><span data-stu-id="3d169-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d169-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="3d169-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d169-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3d169-107">DESCRIPTION</span></span>
<span data-ttu-id="3d169-108">A **Set-AzCurrentStorageAccount** parancsmag módosítja a megadott Azure-előfizetés aktuális Azure-tárfiókját az Azure PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="3d169-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="3d169-109">A rendszer az aktuális tárfiókot használja alapértelmezettként, amikor tárfióknév megadása nélkül fér hozzá a Tárterülethez.</span><span class="sxs-lookup"><span data-stu-id="3d169-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="3d169-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3d169-110">EXAMPLES</span></span>

### <span data-ttu-id="3d169-111">1. példa: Az aktuális tárfiók beállítása</span><span class="sxs-lookup"><span data-stu-id="3d169-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="3d169-112">Ez a parancs beállítja a megadott előfizetés alapértelmezett tárfiókját.</span><span class="sxs-lookup"><span data-stu-id="3d169-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="3d169-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d169-113">PARAMETERS</span></span>

### <span data-ttu-id="3d169-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3d169-114">-Context</span></span>
<span data-ttu-id="3d169-115">Az aktuális **Tárfiók AzureStorageContext** objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d169-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="3d169-116">Tárterület-környezetobjektum beszerzéséhez használja a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3d169-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UsingStorageContext
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d169-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d169-117">-DefaultProfile</span></span>
<span data-ttu-id="3d169-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d169-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d169-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3d169-119">-Name</span></span>
<span data-ttu-id="3d169-120">Annak a tárfióknak a nevét adja meg, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="3d169-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d169-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d169-121">-ResourceGroupName</span></span>
<span data-ttu-id="3d169-122">Azt az erőforráscsoportot adja meg, amely a módosítani kívánt tárfiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3d169-122">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d169-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d169-123">CommonParameters</span></span>
<span data-ttu-id="3d169-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d169-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d169-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d169-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d169-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d169-126">INPUTS</span></span>

### <span data-ttu-id="3d169-127">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3d169-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="3d169-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3d169-128">System.String</span></span>

## <span data-ttu-id="3d169-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d169-129">OUTPUTS</span></span>

### <span data-ttu-id="3d169-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3d169-130">System.String</span></span>

## <span data-ttu-id="3d169-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3d169-131">NOTES</span></span>

## <span data-ttu-id="3d169-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d169-132">RELATED LINKS</span></span>

[<span data-ttu-id="3d169-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d169-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


