---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 23f1ba9185b2a33c910afb0fc7ff0deb2a1cbf5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493530"
---
# <span data-ttu-id="75445-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="75445-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="75445-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75445-102">SYNOPSIS</span></span>
<span data-ttu-id="75445-103">Az adattó-Analytics-fiók törlése</span><span class="sxs-lookup"><span data-stu-id="75445-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75445-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75445-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75445-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="75445-105">DESCRIPTION</span></span>
<span data-ttu-id="75445-106">A **Remove-AzureRmDataLakeAnalyticsAccount** parancsmag véglegesen törli az Azure Data Lake Analytics-fiókját.</span><span class="sxs-lookup"><span data-stu-id="75445-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="75445-107">Példák</span><span class="sxs-lookup"><span data-stu-id="75445-107">EXAMPLES</span></span>

### <span data-ttu-id="75445-108">1. példa: fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="75445-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="75445-109">Ez a parancs eltávolítja a megadott Data Lake Analytics-fiókot.</span><span class="sxs-lookup"><span data-stu-id="75445-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="75445-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75445-110">PARAMETERS</span></span>

### <span data-ttu-id="75445-111">-Force</span><span class="sxs-lookup"><span data-stu-id="75445-111">-Force</span></span>
<span data-ttu-id="75445-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="75445-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75445-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="75445-113">-Name</span></span>
<span data-ttu-id="75445-114">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75445-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="75445-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75445-115">-PassThru</span></span>
<span data-ttu-id="75445-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="75445-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="75445-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="75445-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75445-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75445-118">-ResourceGroupName</span></span>
<span data-ttu-id="75445-119">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75445-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75445-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="75445-120">-Confirm</span></span>
<span data-ttu-id="75445-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="75445-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75445-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75445-122">-WhatIf</span></span>
<span data-ttu-id="75445-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="75445-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75445-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75445-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75445-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75445-125">-DefaultProfile</span></span>
<span data-ttu-id="75445-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75445-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75445-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75445-127">CommonParameters</span></span>
<span data-ttu-id="75445-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75445-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75445-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75445-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75445-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75445-130">INPUTS</span></span>

## <span data-ttu-id="75445-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75445-131">OUTPUTS</span></span>

### <span data-ttu-id="75445-132">bool</span><span class="sxs-lookup"><span data-stu-id="75445-132">bool</span></span>
<span data-ttu-id="75445-133">Ha a PassThru meg van adva, a művelet befejezésekor a True értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="75445-133">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="75445-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75445-134">NOTES</span></span>

## <span data-ttu-id="75445-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75445-135">RELATED LINKS</span></span>

[<span data-ttu-id="75445-136">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="75445-136">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="75445-137">Új – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="75445-137">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="75445-138">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="75445-138">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="75445-139">Teszt-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="75445-139">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


