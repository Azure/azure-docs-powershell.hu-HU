---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: aff12a6bf8c5cfeb79186eef7df0880b9225d433
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298061"
---
# <span data-ttu-id="45fcb-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="45fcb-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="45fcb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="45fcb-103">Az adattó-Analytics-fiók törlése</span><span class="sxs-lookup"><span data-stu-id="45fcb-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="45fcb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45fcb-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45fcb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45fcb-105">DESCRIPTION</span></span>
<span data-ttu-id="45fcb-106">A **Remove-AzDataLakeAnalyticsAccount** parancsmag véglegesen törli az Azure Data Lake Analytics-fiókját.</span><span class="sxs-lookup"><span data-stu-id="45fcb-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="45fcb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="45fcb-107">EXAMPLES</span></span>

### <span data-ttu-id="45fcb-108">1. példa: fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="45fcb-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="45fcb-109">Ez a parancs eltávolítja a megadott Data Lake Analytics-fiókot.</span><span class="sxs-lookup"><span data-stu-id="45fcb-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="45fcb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45fcb-110">PARAMETERS</span></span>

### <span data-ttu-id="45fcb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45fcb-111">-DefaultProfile</span></span>
<span data-ttu-id="45fcb-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="45fcb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45fcb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="45fcb-113">-Force</span></span>
<span data-ttu-id="45fcb-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="45fcb-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45fcb-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45fcb-115">-Name</span></span>
<span data-ttu-id="45fcb-116">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45fcb-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="45fcb-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45fcb-117">-PassThru</span></span>
<span data-ttu-id="45fcb-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="45fcb-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="45fcb-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="45fcb-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="45fcb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45fcb-120">-ResourceGroupName</span></span>
<span data-ttu-id="45fcb-121">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45fcb-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="45fcb-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45fcb-122">-Confirm</span></span>
<span data-ttu-id="45fcb-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45fcb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45fcb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45fcb-124">-WhatIf</span></span>
<span data-ttu-id="45fcb-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45fcb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45fcb-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45fcb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45fcb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45fcb-127">CommonParameters</span></span>
<span data-ttu-id="45fcb-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45fcb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45fcb-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45fcb-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45fcb-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45fcb-130">INPUTS</span></span>

### <span data-ttu-id="45fcb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="45fcb-131">System.String</span></span>

## <span data-ttu-id="45fcb-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45fcb-132">OUTPUTS</span></span>

### <span data-ttu-id="45fcb-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45fcb-133">System.Boolean</span></span>

## <span data-ttu-id="45fcb-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45fcb-134">NOTES</span></span>

## <span data-ttu-id="45fcb-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45fcb-135">RELATED LINKS</span></span>

[<span data-ttu-id="45fcb-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="45fcb-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="45fcb-137">Új – AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="45fcb-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="45fcb-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="45fcb-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="45fcb-139">Teszt-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="45fcb-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


