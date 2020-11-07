---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermcurrentstorageaccount
schema: 2.0.0
ms.openlocfilehash: 134af70c3f913d0eec8310f83341de8784f30f25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848977"
---
# <span data-ttu-id="4b723-101">Set-AzureRmCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4b723-101">Set-AzureRmCurrentStorageAccount</span></span>

## <span data-ttu-id="4b723-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b723-102">SYNOPSIS</span></span>
<span data-ttu-id="4b723-103">Módosítja a megadott előfizetés jelenlegi tárterület-fiókját.</span><span class="sxs-lookup"><span data-stu-id="4b723-103">Modifies the current Storage account of the specified subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b723-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b723-104">SYNTAX</span></span>

### <span data-ttu-id="4b723-105">UsingResourceGroupAndNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4b723-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b723-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="4b723-106">UsingStorageContext</span></span>
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b723-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b723-107">DESCRIPTION</span></span>
<span data-ttu-id="4b723-108">A **set-AzureRmCurrentStorageAccount** parancsmag a megadott Azure-előfizetés jelenlegi Azure Storage-fiókját módosítja az Azure PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="4b723-108">The **Set-AzureRmCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="4b723-109">Az aktuális tárterület-fiók alapértelmezés szerint akkor használható, ha a tárterületet a tárolási Fióknév megadása nélkül éri el.</span><span class="sxs-lookup"><span data-stu-id="4b723-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="4b723-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4b723-110">EXAMPLES</span></span>

### <span data-ttu-id="4b723-111">1. példa: az aktuális tárterület-fiók beállítása</span><span class="sxs-lookup"><span data-stu-id="4b723-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="4b723-112">Ez a parancs beállítja a megadott előfizetés alapértelmezett tárolási fiókját.</span><span class="sxs-lookup"><span data-stu-id="4b723-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="4b723-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b723-113">PARAMETERS</span></span>

### <span data-ttu-id="4b723-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4b723-114">-Context</span></span>
<span data-ttu-id="4b723-115">Az aktuális tárterület-fiók **AzureStorageContext** -objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b723-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="4b723-116">A tárolási környezet-objektum beolvasásához használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4b723-116">To obtain a storage context object, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4b723-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b723-117">-DefaultProfile</span></span>
<span data-ttu-id="4b723-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b723-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b723-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4b723-119">-Name</span></span>
<span data-ttu-id="4b723-120">Annak a tároló fióknak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="4b723-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4b723-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b723-121">-ResourceGroupName</span></span>
<span data-ttu-id="4b723-122">Azt a erőforráscsoportot adja meg, amely a módosítani kívánt tárolási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4b723-122">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="4b723-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b723-123">CommonParameters</span></span>
<span data-ttu-id="4b723-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b723-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b723-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b723-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b723-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b723-126">INPUTS</span></span>

### <span data-ttu-id="4b723-127">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4b723-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="4b723-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4b723-128">System.String</span></span>

## <span data-ttu-id="4b723-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b723-129">OUTPUTS</span></span>

### <span data-ttu-id="4b723-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4b723-130">System.String</span></span>

## <span data-ttu-id="4b723-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b723-131">NOTES</span></span>

## <span data-ttu-id="4b723-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b723-132">RELATED LINKS</span></span>

[<span data-ttu-id="4b723-133">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4b723-133">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


