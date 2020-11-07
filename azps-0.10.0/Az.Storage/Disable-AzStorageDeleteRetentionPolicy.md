---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f09ba3cdd0404f1eca21540a6893f1bcd67f05e5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843134"
---
# <span data-ttu-id="d5dda-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d5dda-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="d5dda-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5dda-102">SYNOPSIS</span></span>
<span data-ttu-id="d5dda-103">Tiltsa le a törlés adatmegőrzési házirendet az Azure Storage blob szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="d5dda-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="d5dda-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5dda-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5dda-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5dda-105">DESCRIPTION</span></span>
<span data-ttu-id="d5dda-106">A **disable-AzStorageDeleteRetentionPolicy** parancsmag letiltja a törlés-adatmegőrzési házirendet az Azure Storage blob szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="d5dda-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="d5dda-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d5dda-107">EXAMPLES</span></span>

### <span data-ttu-id="d5dda-108">1. példa: a blob-szolgáltatás adatmegőrzési házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="d5dda-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="d5dda-109">Ez a parancs letiltja a blob-szolgáltatás adatmegőrzési házirendjének törlését.</span><span class="sxs-lookup"><span data-stu-id="d5dda-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="d5dda-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5dda-110">PARAMETERS</span></span>

### <span data-ttu-id="d5dda-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d5dda-111">-Context</span></span>
<span data-ttu-id="d5dda-112">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="d5dda-112">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5dda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5dda-113">-DefaultProfile</span></span>
<span data-ttu-id="d5dda-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5dda-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5dda-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5dda-115">-PassThru</span></span>
<span data-ttu-id="d5dda-116">DeleteRetentionPolicyProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="d5dda-116">Display DeleteRetentionPolicyProperties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5dda-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d5dda-117">-Confirm</span></span>
<span data-ttu-id="d5dda-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d5dda-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5dda-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5dda-119">-WhatIf</span></span>
<span data-ttu-id="d5dda-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d5dda-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5dda-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d5dda-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5dda-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5dda-122">CommonParameters</span></span>
<span data-ttu-id="d5dda-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5dda-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5dda-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5dda-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5dda-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5dda-125">INPUTS</span></span>

### <span data-ttu-id="d5dda-126">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d5dda-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d5dda-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5dda-127">OUTPUTS</span></span>

### <span data-ttu-id="d5dda-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d5dda-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="d5dda-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5dda-129">NOTES</span></span>

## <span data-ttu-id="d5dda-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5dda-130">RELATED LINKS</span></span>
