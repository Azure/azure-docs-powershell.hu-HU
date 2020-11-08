---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CD2274E5-B3D4-489E-B374-8B2BCC1F923E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90666be18ee3e546620d0c10386594b8ae7ec8a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016235"
---
# <span data-ttu-id="deac5-101">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="deac5-101">New-AzureAclConfig</span></span>

## <span data-ttu-id="deac5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="deac5-102">SYNOPSIS</span></span>
<span data-ttu-id="deac5-103">Üres ACL-konfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="deac5-103">Creates an empty ACL configuration object.</span></span>

## <span data-ttu-id="deac5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="deac5-104">SYNTAX</span></span>

```
New-AzureAclConfig [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="deac5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="deac5-105">DESCRIPTION</span></span>
<span data-ttu-id="deac5-106">A **New-AzureAclConfig** parancsmag üres hozzáférés-vezérlési lista (ACL) konfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="deac5-106">The **New-AzureAclConfig** cmdlet creates an empty access control list (ACL) configuration object.</span></span>

## <span data-ttu-id="deac5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="deac5-107">EXAMPLES</span></span>

### <span data-ttu-id="deac5-108">Példa 1: ACL-konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="deac5-108">Example 1: Create an ACL configuration object</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
```

<span data-ttu-id="deac5-109">Ez a parancs létrehoz egy üres ACL-konfigurációs objektumot, majd a $Acl változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="deac5-109">This command creates an empty ACL configuration object, and then stores it in the $Acl variable.</span></span>

## <span data-ttu-id="deac5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="deac5-110">PARAMETERS</span></span>

### <span data-ttu-id="deac5-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="deac5-111">-InformationAction</span></span>
<span data-ttu-id="deac5-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="deac5-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="deac5-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="deac5-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="deac5-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="deac5-114">Continue</span></span>
- <span data-ttu-id="deac5-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="deac5-115">Ignore</span></span>
- <span data-ttu-id="deac5-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="deac5-116">Inquire</span></span>
- <span data-ttu-id="deac5-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="deac5-117">SilentlyContinue</span></span>
- <span data-ttu-id="deac5-118">állj</span><span class="sxs-lookup"><span data-stu-id="deac5-118">Stop</span></span>
- <span data-ttu-id="deac5-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="deac5-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deac5-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="deac5-120">-InformationVariable</span></span>
<span data-ttu-id="deac5-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="deac5-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deac5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deac5-122">CommonParameters</span></span>
<span data-ttu-id="deac5-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="deac5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deac5-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deac5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deac5-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="deac5-125">INPUTS</span></span>

## <span data-ttu-id="deac5-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="deac5-126">OUTPUTS</span></span>

## <span data-ttu-id="deac5-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="deac5-127">NOTES</span></span>

## <span data-ttu-id="deac5-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="deac5-128">RELATED LINKS</span></span>

[<span data-ttu-id="deac5-129">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="deac5-129">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="deac5-130">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="deac5-130">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="deac5-131">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="deac5-131">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


