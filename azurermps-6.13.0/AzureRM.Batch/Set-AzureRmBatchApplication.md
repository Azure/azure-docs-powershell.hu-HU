---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
ms.openlocfilehash: 8ede896e6a49cee5305e7f9fd42f6dab130e7986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498407"
---
# <span data-ttu-id="9dc09-101">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="9dc09-101">Set-AzureRmBatchApplication</span></span>

## <span data-ttu-id="9dc09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9dc09-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc09-103">A megadott alkalmazás frissítési beállításai.</span><span class="sxs-lookup"><span data-stu-id="9dc09-103">Updates settings for the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dc09-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9dc09-104">SYNTAX</span></span>

```
Set-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dc09-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9dc09-105">DESCRIPTION</span></span>
<span data-ttu-id="9dc09-106">A **set-AzureRmBatchApplication** parancsmag a megadott Azure kötegfájl-alkalmazás beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="9dc09-106">The **Set-AzureRmBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="9dc09-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9dc09-107">EXAMPLES</span></span>

### <span data-ttu-id="9dc09-108">Példa 1: az alkalmazás frissítése egy köteg fiókban</span><span class="sxs-lookup"><span data-stu-id="9dc09-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="9dc09-109">Ez a parancs azt módosítja, hogy az ContosoBatch-fiók Llitware alkalmazása engedélyezi-e a frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="9dc09-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="9dc09-110">A parancs nem módosítja az alkalmazás alapértelmezett verzióját vagy megjelenítendő nevét.</span><span class="sxs-lookup"><span data-stu-id="9dc09-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="9dc09-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9dc09-111">PARAMETERS</span></span>

### <span data-ttu-id="9dc09-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9dc09-112">-AccountName</span></span>
<span data-ttu-id="9dc09-113">Annak a kötegelt fióknak a nevét adja meg, amelyhez ez a parancsmag módosított egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="9dc09-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="9dc09-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="9dc09-114">-AllowUpdates</span></span>
<span data-ttu-id="9dc09-115">Itt adhatja meg, hogy az alkalmazásban lévő csomagokat felülírja-e ugyanazzal a verziójú karakterlánccal.</span><span class="sxs-lookup"><span data-stu-id="9dc09-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc09-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9dc09-116">-ApplicationId</span></span>
<span data-ttu-id="9dc09-117">Az alkalmazás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9dc09-117">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc09-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc09-118">-DefaultProfile</span></span>
<span data-ttu-id="9dc09-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9dc09-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dc09-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="9dc09-120">-DefaultVersion</span></span>
<span data-ttu-id="9dc09-121">Annak megadása, hogy melyik csomagot használja, ha egy ügyfél kéri az alkalmazást, de nem ad meg verziót.</span><span class="sxs-lookup"><span data-stu-id="9dc09-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc09-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9dc09-122">-DisplayName</span></span>
<span data-ttu-id="9dc09-123">Az alkalmazás megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9dc09-123">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc09-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dc09-124">-ResourceGroupName</span></span>
<span data-ttu-id="9dc09-125">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9dc09-125">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc09-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc09-126">CommonParameters</span></span>
<span data-ttu-id="9dc09-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9dc09-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc09-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dc09-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc09-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dc09-129">INPUTS</span></span>

### <span data-ttu-id="9dc09-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9dc09-130">System.String</span></span>

### <span data-ttu-id="9dc09-131">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9dc09-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9dc09-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dc09-132">OUTPUTS</span></span>

### <span data-ttu-id="9dc09-133">System. Void</span><span class="sxs-lookup"><span data-stu-id="9dc09-133">System.Void</span></span>

## <span data-ttu-id="9dc09-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9dc09-134">NOTES</span></span>

## <span data-ttu-id="9dc09-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9dc09-135">RELATED LINKS</span></span>

[<span data-ttu-id="9dc09-136">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="9dc09-136">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="9dc09-137">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="9dc09-137">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="9dc09-138">Új – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="9dc09-138">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="9dc09-139">Új – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="9dc09-139">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="9dc09-140">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="9dc09-140">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="9dc09-141">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="9dc09-141">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)


