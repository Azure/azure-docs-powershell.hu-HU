---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
ms.openlocfilehash: 73680e82a9d898075e905d88bcc8602609a5612d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672673"
---
# <span data-ttu-id="63963-101">Set-AzureRmCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="63963-101">Set-AzureRmCurrentStorageAccount</span></span>

## <span data-ttu-id="63963-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63963-102">SYNOPSIS</span></span>
<span data-ttu-id="63963-103">Módosítja a megadott előfizetés jelenlegi tárterület-fiókját.</span><span class="sxs-lookup"><span data-stu-id="63963-103">Modifies the current Storage account of the specified subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63963-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63963-104">SYNTAX</span></span>

### <span data-ttu-id="63963-105">UsingResourceGroupAndNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="63963-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63963-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="63963-106">UsingStorageContext</span></span>
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63963-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="63963-107">DESCRIPTION</span></span>
<span data-ttu-id="63963-108">A **set-AzureRmCurrentStorageAccount** parancsmag a megadott Azure-előfizetés jelenlegi Azure Storage-fiókját módosítja az Azure PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="63963-108">The **Set-AzureRmCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="63963-109">Az aktuális tárterület-fiók alapértelmezés szerint akkor használható, ha a tárterületet a tárolási Fióknév megadása nélkül éri el.</span><span class="sxs-lookup"><span data-stu-id="63963-109">The current storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="63963-110">Példák</span><span class="sxs-lookup"><span data-stu-id="63963-110">EXAMPLES</span></span>

### <span data-ttu-id="63963-111">1. példa: az aktuális tárterület-fiók beállítása</span><span class="sxs-lookup"><span data-stu-id="63963-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="63963-112">Ez a parancs beállítja a megadott előfizetés alapértelmezett tárolási fiókját.</span><span class="sxs-lookup"><span data-stu-id="63963-112">This command sets the default storage account for the specified subscription.</span></span>

## <span data-ttu-id="63963-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63963-113">PARAMETERS</span></span>

### <span data-ttu-id="63963-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="63963-114">-Context</span></span>
<span data-ttu-id="63963-115">Az aktuális tárterület-fiók **AzureStorageContext** -objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="63963-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="63963-116">A tárolási környezet-objektum beolvasásához használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="63963-116">To obtain a storage context object, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="63963-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="63963-117">-Name</span></span>
<span data-ttu-id="63963-118">Annak a tároló fióknak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="63963-118">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="63963-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63963-119">-ResourceGroupName</span></span>
<span data-ttu-id="63963-120">Azt a erőforráscsoportot adja meg, amely a módosítani kívánt tárolási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="63963-120">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="63963-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63963-121">-DefaultProfile</span></span>
<span data-ttu-id="63963-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63963-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63963-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63963-123">CommonParameters</span></span>
<span data-ttu-id="63963-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63963-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63963-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63963-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63963-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63963-126">INPUTS</span></span>

## <span data-ttu-id="63963-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63963-127">OUTPUTS</span></span>

## <span data-ttu-id="63963-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63963-128">NOTES</span></span>

## <span data-ttu-id="63963-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63963-129">RELATED LINKS</span></span>

[<span data-ttu-id="63963-130">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="63963-130">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


