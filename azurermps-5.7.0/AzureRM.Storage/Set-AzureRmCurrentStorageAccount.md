---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermcurrentstorageaccount
schema: 2.0.0
ms.openlocfilehash: 6a7ef50e6e95a30140549343d14d4a75ad340cbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679245"
---
# <span data-ttu-id="223c0-101">Set-AzureRmCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="223c0-101">Set-AzureRmCurrentStorageAccount</span></span>

## <span data-ttu-id="223c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="223c0-102">SYNOPSIS</span></span>
<span data-ttu-id="223c0-103">Módosítja a megadott előfizetés jelenlegi tárterület-fiókját.</span><span class="sxs-lookup"><span data-stu-id="223c0-103">Modifies the current Storage account of the specified subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="223c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="223c0-104">SYNTAX</span></span>

### <span data-ttu-id="223c0-105">UsingResourceGroupAndNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="223c0-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="223c0-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="223c0-106">UsingStorageContext</span></span>
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="223c0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="223c0-107">DESCRIPTION</span></span>
<span data-ttu-id="223c0-108">A **set-AzureRmCurrentStorageAccount** parancsmag a megadott Azure-előfizetés jelenlegi Azure Storage-fiókját módosítja az Azure PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="223c0-108">The **Set-AzureRmCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="223c0-109">Az aktuális tárterület-fiók alapértelmezés szerint akkor használható, ha a tárterületet a tárolási Fióknév megadása nélkül éri el.</span><span class="sxs-lookup"><span data-stu-id="223c0-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="223c0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="223c0-110">EXAMPLES</span></span>

### <span data-ttu-id="223c0-111">1. példa: az aktuális tárterület-fiók beállítása</span><span class="sxs-lookup"><span data-stu-id="223c0-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="223c0-112">Ez a parancs beállítja a megadott előfizetés alapértelmezett tárolási fiókját.</span><span class="sxs-lookup"><span data-stu-id="223c0-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="223c0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="223c0-113">PARAMETERS</span></span>

### <span data-ttu-id="223c0-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="223c0-114">-Context</span></span>
<span data-ttu-id="223c0-115">Az aktuális tárterület-fiók **AzureStorageContext** -objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="223c0-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="223c0-116">A tárolási környezet-objektum beolvasásához használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="223c0-116">To obtain a storage context object, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: UsingStorageContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="223c0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="223c0-117">-DefaultProfile</span></span>
<span data-ttu-id="223c0-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="223c0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="223c0-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="223c0-119">-Name</span></span>
<span data-ttu-id="223c0-120">Annak a tároló fióknak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="223c0-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="223c0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="223c0-121">-ResourceGroupName</span></span>
<span data-ttu-id="223c0-122">Azt a erőforráscsoportot adja meg, amely a módosítani kívánt tárolási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="223c0-122">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="223c0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="223c0-123">CommonParameters</span></span>
<span data-ttu-id="223c0-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="223c0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="223c0-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="223c0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="223c0-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="223c0-126">INPUTS</span></span>

### <span data-ttu-id="223c0-127">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="223c0-127">IStorageContext</span></span>
<span data-ttu-id="223c0-128">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="223c0-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="223c0-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="223c0-129">OUTPUTS</span></span>

### <span data-ttu-id="223c0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="223c0-130">System.String</span></span>

## <span data-ttu-id="223c0-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="223c0-131">NOTES</span></span>

## <span data-ttu-id="223c0-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="223c0-132">RELATED LINKS</span></span>

[<span data-ttu-id="223c0-133">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="223c0-133">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


