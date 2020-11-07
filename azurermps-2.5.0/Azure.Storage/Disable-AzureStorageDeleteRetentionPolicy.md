---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
ms.openlocfilehash: d899b34e2f880a0351ce4d10f360f7bc29011b0c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849457"
---
# <span data-ttu-id="83687-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="83687-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="83687-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83687-102">SYNOPSIS</span></span>
<span data-ttu-id="83687-103">Tiltsa le a törlés adatmegőrzési házirendet az Azure Storage blob szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="83687-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83687-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83687-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83687-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="83687-105">DESCRIPTION</span></span>
<span data-ttu-id="83687-106">A **disable-AzureStorageDeleteRetentionPolicy** parancsmag letiltja a törlés-adatmegőrzési házirendet az Azure Storage blob szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="83687-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="83687-107">Példák</span><span class="sxs-lookup"><span data-stu-id="83687-107">EXAMPLES</span></span>

### <span data-ttu-id="83687-108">1. példa: a blob-szolgáltatás adatmegőrzési házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="83687-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="83687-109">Ez a parancs letiltja a blob-szolgáltatás adatmegőrzési házirendjének törlését.</span><span class="sxs-lookup"><span data-stu-id="83687-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="83687-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83687-110">PARAMETERS</span></span>

### <span data-ttu-id="83687-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="83687-111">-Context</span></span>
<span data-ttu-id="83687-112">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="83687-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="83687-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83687-113">-DefaultProfile</span></span>
<span data-ttu-id="83687-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83687-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83687-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83687-115">-PassThru</span></span>
<span data-ttu-id="83687-116">DeleteRetentionPolicyProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="83687-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="83687-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83687-117">-Confirm</span></span>
<span data-ttu-id="83687-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83687-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83687-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83687-119">-WhatIf</span></span>
<span data-ttu-id="83687-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83687-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83687-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83687-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83687-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83687-122">CommonParameters</span></span>
<span data-ttu-id="83687-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83687-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83687-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83687-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83687-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83687-125">INPUTS</span></span>

### <span data-ttu-id="83687-126">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="83687-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="83687-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83687-127">OUTPUTS</span></span>

### <span data-ttu-id="83687-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="83687-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="83687-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83687-129">NOTES</span></span>

## <span data-ttu-id="83687-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83687-130">RELATED LINKS</span></span>
