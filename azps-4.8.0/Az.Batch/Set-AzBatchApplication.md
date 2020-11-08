---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
ms.openlocfilehash: 6d6c72702d03b3b2174c21c786fb373374cea739
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024889"
---
# <span data-ttu-id="522ac-101">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="522ac-101">Set-AzBatchApplication</span></span>

## <span data-ttu-id="522ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="522ac-102">SYNOPSIS</span></span>
<span data-ttu-id="522ac-103">A megadott alkalmazás frissítési beállításai.</span><span class="sxs-lookup"><span data-stu-id="522ac-103">Updates settings for the specified application.</span></span>

## <span data-ttu-id="522ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="522ac-104">SYNTAX</span></span>

```
Set-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="522ac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="522ac-105">DESCRIPTION</span></span>
<span data-ttu-id="522ac-106">A **set-AzBatchApplication** parancsmag a megadott Azure kötegfájl-alkalmazás beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="522ac-106">The **Set-AzBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="522ac-107">Példák</span><span class="sxs-lookup"><span data-stu-id="522ac-107">EXAMPLES</span></span>

### <span data-ttu-id="522ac-108">Példa 1: az alkalmazás frissítése egy köteg fiókban</span><span class="sxs-lookup"><span data-stu-id="522ac-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $False
```

<span data-ttu-id="522ac-109">Ez a parancs azt módosítja, hogy az ContosoBatch-fiók Bárdos Iparcikk alkalmazása engedélyezi-e a frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="522ac-109">This command changes whether the Litware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="522ac-110">A parancs nem módosítja az alkalmazás alapértelmezett verzióját vagy megjelenítendő nevét.</span><span class="sxs-lookup"><span data-stu-id="522ac-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="522ac-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="522ac-111">PARAMETERS</span></span>

### <span data-ttu-id="522ac-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="522ac-112">-AccountName</span></span>
<span data-ttu-id="522ac-113">Annak a kötegelt fióknak a nevét adja meg, amelyhez ez a parancsmag módosított egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="522ac-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="522ac-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="522ac-114">-AllowUpdates</span></span>
<span data-ttu-id="522ac-115">Itt adhatja meg, hogy az alkalmazásban lévő csomagokat felülírja-e ugyanazzal a verziójú karakterlánccal.</span><span class="sxs-lookup"><span data-stu-id="522ac-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="522ac-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="522ac-116">-ApplicationName</span></span>
<span data-ttu-id="522ac-117">Az alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="522ac-117">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="522ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="522ac-118">-DefaultProfile</span></span>
<span data-ttu-id="522ac-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="522ac-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="522ac-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="522ac-120">-DefaultVersion</span></span>
<span data-ttu-id="522ac-121">Annak megadása, hogy melyik csomagot használja, ha egy ügyfél kéri az alkalmazást, de nem ad meg verziót.</span><span class="sxs-lookup"><span data-stu-id="522ac-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="522ac-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="522ac-122">-DisplayName</span></span>
<span data-ttu-id="522ac-123">Az alkalmazás megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="522ac-123">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="522ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="522ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="522ac-125">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="522ac-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="522ac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="522ac-126">CommonParameters</span></span>
<span data-ttu-id="522ac-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="522ac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="522ac-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="522ac-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="522ac-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="522ac-129">INPUTS</span></span>

### <span data-ttu-id="522ac-130">System. String</span><span class="sxs-lookup"><span data-stu-id="522ac-130">System.String</span></span>

### <span data-ttu-id="522ac-131">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="522ac-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="522ac-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="522ac-132">OUTPUTS</span></span>

### <span data-ttu-id="522ac-133">System. Void</span><span class="sxs-lookup"><span data-stu-id="522ac-133">System.Void</span></span>

## <span data-ttu-id="522ac-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="522ac-134">NOTES</span></span>

## <span data-ttu-id="522ac-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="522ac-135">RELATED LINKS</span></span>

[<span data-ttu-id="522ac-136">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="522ac-136">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="522ac-137">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="522ac-137">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="522ac-138">Új – AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="522ac-138">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="522ac-139">Új – AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="522ac-139">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="522ac-140">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="522ac-140">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="522ac-141">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="522ac-141">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)


