---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: 24c0140f4a1ba09111db0dacaa612c4a635493fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668549"
---
# <span data-ttu-id="0115f-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0115f-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="0115f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0115f-102">SYNOPSIS</span></span>
<span data-ttu-id="0115f-103">Módosítja a megadott előfizetés jelenlegi tárterület-fiókját.</span><span class="sxs-lookup"><span data-stu-id="0115f-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="0115f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0115f-104">SYNTAX</span></span>

### <span data-ttu-id="0115f-105">UsingResourceGroupAndNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0115f-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0115f-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="0115f-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0115f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0115f-107">DESCRIPTION</span></span>
<span data-ttu-id="0115f-108">A **set-AzCurrentStorageAccount** parancsmag a megadott Azure-előfizetés jelenlegi Azure Storage-fiókját módosítja az Azure PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="0115f-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="0115f-109">Az aktuális tárterület-fiók alapértelmezés szerint akkor használható, ha a tárterületet a tárolási Fióknév megadása nélkül éri el.</span><span class="sxs-lookup"><span data-stu-id="0115f-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="0115f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0115f-110">EXAMPLES</span></span>

### <span data-ttu-id="0115f-111">1. példa: az aktuális tárterület-fiók beállítása</span><span class="sxs-lookup"><span data-stu-id="0115f-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="0115f-112">Ez a parancs beállítja a megadott előfizetés alapértelmezett tárolási fiókját.</span><span class="sxs-lookup"><span data-stu-id="0115f-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="0115f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0115f-113">PARAMETERS</span></span>

### <span data-ttu-id="0115f-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0115f-114">-Context</span></span>
<span data-ttu-id="0115f-115">Az aktuális tárterület-fiók **AzureStorageContext** -objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0115f-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="0115f-116">A tárolási környezet-objektum beolvasásához használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0115f-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0115f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0115f-117">-DefaultProfile</span></span>
<span data-ttu-id="0115f-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0115f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0115f-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0115f-119">-Name</span></span>
<span data-ttu-id="0115f-120">Annak a tároló fióknak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="0115f-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0115f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0115f-121">-ResourceGroupName</span></span>
<span data-ttu-id="0115f-122">Azt a erőforráscsoportot adja meg, amely a módosítani kívánt tárolási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0115f-122">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="0115f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0115f-123">CommonParameters</span></span>
<span data-ttu-id="0115f-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0115f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0115f-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0115f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0115f-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0115f-126">INPUTS</span></span>

### <span data-ttu-id="0115f-127">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0115f-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="0115f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0115f-128">System.String</span></span>

## <span data-ttu-id="0115f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0115f-129">OUTPUTS</span></span>

### <span data-ttu-id="0115f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0115f-130">System.String</span></span>

## <span data-ttu-id="0115f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0115f-131">NOTES</span></span>

## <span data-ttu-id="0115f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0115f-132">RELATED LINKS</span></span>

[<span data-ttu-id="0115f-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0115f-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


