---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015448"
---
# <span data-ttu-id="336d7-101">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="336d7-101">Select-AzureStorSimpleResource</span></span>

## <span data-ttu-id="336d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="336d7-102">SYNOPSIS</span></span>
<span data-ttu-id="336d7-103">Erőforrást állít be aktuális erőforrásként.</span><span class="sxs-lookup"><span data-stu-id="336d7-103">Sets a resource as the current resource.</span></span>

## <span data-ttu-id="336d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="336d7-104">SYNTAX</span></span>

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="336d7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="336d7-105">DESCRIPTION</span></span>
<span data-ttu-id="336d7-106">A **Select-AzureStorSimpleResource** parancsmag aktuális erőforrásként állítja be az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="336d7-106">The **Select-AzureStorSimpleResource** cmdlet sets a resource as the current resource.</span></span>
<span data-ttu-id="336d7-107">Miután kiválasztott egy erőforrást, az egyéb parancsmagok az adott erőforrás környezetén belül érvényesek.</span><span class="sxs-lookup"><span data-stu-id="336d7-107">After you select a resource, other cmdlets apply within that resource context.</span></span>

## <span data-ttu-id="336d7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="336d7-108">EXAMPLES</span></span>

### <span data-ttu-id="336d7-109">1. példa: erőforrás kijelölése első alkalommal</span><span class="sxs-lookup"><span data-stu-id="336d7-109">Example 1: Select a resource for the first time</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="336d7-110">A parancs kijelöli az Contoso64-Tsqa nevű erőforrást az aktuális környezetben.</span><span class="sxs-lookup"><span data-stu-id="336d7-110">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="336d7-111">Ebben a példában a számítógépen nem volt ilyen környezet inicializálva korábban, ezért a *RegistrationKey* paraméter értékét is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="336d7-111">In this example, the computer has not had this context initialized previously, and, therefore, you must specify a value for the *RegistrationKey* parameter.</span></span>

### <span data-ttu-id="336d7-112">2. példa: erőforrás kiválasztásának kísérlete</span><span class="sxs-lookup"><span data-stu-id="336d7-112">Example 2: Attempt to select a resource</span></span>
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### <span data-ttu-id="336d7-113">3. példa: egy korábban kijelölt erőforrás kijelölése</span><span class="sxs-lookup"><span data-stu-id="336d7-113">Example 3: Select a previously selected resource</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="336d7-114">A parancs kijelöli az Contoso64-Tsqa nevű erőforrást az aktuális környezetben.</span><span class="sxs-lookup"><span data-stu-id="336d7-114">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="336d7-115">Ebben a példában ez a környezet korábban ki volt jelölve, ezért nem kell megadni a *RegistrationKey* paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="336d7-115">In this example, that context has previously been selected, and, therefore, you do not need to specify a value for the *RegistrationKey* parameter.</span></span>

## <span data-ttu-id="336d7-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="336d7-116">PARAMETERS</span></span>

### <span data-ttu-id="336d7-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="336d7-117">-Profile</span></span>
<span data-ttu-id="336d7-118">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="336d7-118">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336d7-119">-RegistrationKey</span><span class="sxs-lookup"><span data-stu-id="336d7-119">-RegistrationKey</span></span>
<span data-ttu-id="336d7-120">A regisztrációs kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="336d7-120">Specifies a registration key.</span></span>
<span data-ttu-id="336d7-121">Adjon meg egy billentyűt az első alkalommal, amikor kijelöl egy erőforrást.</span><span class="sxs-lookup"><span data-stu-id="336d7-121">Specify a key the first time that you select a resource.</span></span>
<span data-ttu-id="336d7-122">Miután a parancsmag kijelöli az aktuális erőforrást, a parancsmagok szükség szerint ezt a billentyűt használják.</span><span class="sxs-lookup"><span data-stu-id="336d7-122">After this cmdlet selects the current resource, cmdlets use this key, as required.</span></span>
<span data-ttu-id="336d7-123">További információt a [szolgáltatás regisztrációs kulcsának beszerzése](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  ( https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) a Microsoft fejlesztői hálózatán) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="336d7-123">For more information, see [Get the service registration key](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  (https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) on the Microsoft Developer Network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336d7-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="336d7-124">-ResourceName</span></span>
<span data-ttu-id="336d7-125">Annak az erőforrásnak a nevét adja meg, amelyet az aktuális erőforrásként szeretne kijelölni.</span><span class="sxs-lookup"><span data-stu-id="336d7-125">Specifies the name of the resource to select as the current resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336d7-126">CommonParameters</span></span>
<span data-ttu-id="336d7-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="336d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336d7-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="336d7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336d7-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="336d7-129">INPUTS</span></span>

### <span data-ttu-id="336d7-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="336d7-130">None</span></span>

## <span data-ttu-id="336d7-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="336d7-131">OUTPUTS</span></span>

### <span data-ttu-id="336d7-132">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="336d7-132">StorSimpleResourceContext</span></span>
<span data-ttu-id="336d7-133">Ez a parancsmag egy **StorSimpleResourceContext** objektumot ad eredményül, amely tartalmazza az erőforrás környezetének részleteit.</span><span class="sxs-lookup"><span data-stu-id="336d7-133">This cmdlet returns a **StorSimpleResourceContext** object that contains details for the resource context.</span></span>

## <span data-ttu-id="336d7-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="336d7-134">NOTES</span></span>

## <span data-ttu-id="336d7-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="336d7-135">RELATED LINKS</span></span>

[<span data-ttu-id="336d7-136">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="336d7-136">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="336d7-137">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="336d7-137">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)


