---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: cd853184e06403f3c0d516ee1b0790c724adacb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501839"
---
# <span data-ttu-id="8c793-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8c793-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="8c793-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c793-102">SYNOPSIS</span></span>
<span data-ttu-id="8c793-103">Az automéretarány beállítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8c793-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c793-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c793-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroup <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c793-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c793-105">DESCRIPTION</span></span>
<span data-ttu-id="8c793-106">A **Remove-AzureRmAutoscaleSetting** parancsmag automatikusan eltávolítja az automéretarány beállítást.</span><span class="sxs-lookup"><span data-stu-id="8c793-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="8c793-107">Meg kell adnia a beállítás nevét, valamint annak az erőforrás-csoportnak a nevét, amelyhez hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="8c793-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

## <span data-ttu-id="8c793-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8c793-108">EXAMPLES</span></span>

## <span data-ttu-id="8c793-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c793-109">PARAMETERS</span></span>

### <span data-ttu-id="8c793-110">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8c793-110">-Name</span></span>
<span data-ttu-id="8c793-111">Az eltávolítandó méretezési beállítás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c793-111">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c793-112">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c793-112">-ResourceGroup</span></span>
<span data-ttu-id="8c793-113">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c793-113">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c793-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c793-114">-DefaultProfile</span></span>
<span data-ttu-id="8c793-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c793-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c793-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c793-116">CommonParameters</span></span>
<span data-ttu-id="8c793-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c793-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c793-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c793-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c793-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c793-119">INPUTS</span></span>

## <span data-ttu-id="8c793-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c793-120">OUTPUTS</span></span>

### <span data-ttu-id="8c793-121">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8c793-121">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="8c793-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c793-122">NOTES</span></span>

## <span data-ttu-id="8c793-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c793-123">RELATED LINKS</span></span>

[<span data-ttu-id="8c793-124">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8c793-124">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="8c793-125">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8c793-125">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


