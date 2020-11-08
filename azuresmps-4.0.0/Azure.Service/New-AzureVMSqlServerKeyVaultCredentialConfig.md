---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EC6F7790-5E31-4C22-B006-38B5C1868671
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0272740ced33d19e2610a6116812df4a815ea3c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016188"
---
# <span data-ttu-id="ed474-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="ed474-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="ed474-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed474-102">SYNOPSIS</span></span>

## <span data-ttu-id="ed474-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed474-103">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed474-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed474-104">DESCRIPTION</span></span>

## <span data-ttu-id="ed474-105">Példák</span><span class="sxs-lookup"><span data-stu-id="ed474-105">EXAMPLES</span></span>

### <span data-ttu-id="ed474-106">1:</span><span class="sxs-lookup"><span data-stu-id="ed474-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="ed474-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed474-107">PARAMETERS</span></span>

### <span data-ttu-id="ed474-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="ed474-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed474-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ed474-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed474-110">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="ed474-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed474-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ed474-111">-InformationAction</span></span>
<span data-ttu-id="ed474-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="ed474-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ed474-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ed474-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ed474-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="ed474-114">Continue</span></span>
- <span data-ttu-id="ed474-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="ed474-115">Ignore</span></span>
- <span data-ttu-id="ed474-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="ed474-116">Inquire</span></span>
- <span data-ttu-id="ed474-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ed474-117">SilentlyContinue</span></span>
- <span data-ttu-id="ed474-118">állj</span><span class="sxs-lookup"><span data-stu-id="ed474-118">Stop</span></span>
- <span data-ttu-id="ed474-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="ed474-119">Suspend</span></span>

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

### <span data-ttu-id="ed474-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ed474-120">-InformationVariable</span></span>
<span data-ttu-id="ed474-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="ed474-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ed474-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="ed474-122">-Profile</span></span>
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

### <span data-ttu-id="ed474-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ed474-123">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed474-124">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="ed474-124">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed474-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed474-125">CommonParameters</span></span>
<span data-ttu-id="ed474-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed474-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed474-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed474-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed474-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed474-128">INPUTS</span></span>

## <span data-ttu-id="ed474-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed474-129">OUTPUTS</span></span>

## <span data-ttu-id="ed474-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed474-130">NOTES</span></span>

## <span data-ttu-id="ed474-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed474-131">RELATED LINKS</span></span>

