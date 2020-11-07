---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35b937b810da65cc3cc2ed330198011ec108f9d6
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/19/2020
ms.locfileid: "93847698"
---
# <span data-ttu-id="f2b77-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="f2b77-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="f2b77-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2b77-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b77-103">Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="f2b77-103">Restore a backup.</span></span>

## <span data-ttu-id="f2b77-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2b77-104">SYNTAX</span></span>

### <span data-ttu-id="f2b77-105">Backups_Restore (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2b77-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>]
 -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2b77-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2b77-106">ResourceId</span></span>
```
Restore-AzsBackup -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2b77-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2b77-107">DESCRIPTION</span></span>
<span data-ttu-id="f2b77-108">Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="f2b77-108">Restore a backup.</span></span>

## <span data-ttu-id="f2b77-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f2b77-109">EXAMPLES</span></span>

### <span data-ttu-id="f2b77-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="f2b77-110">EXAMPLE 1</span></span>
```
Restore-AzsBackup -Name 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword
```

<span data-ttu-id="f2b77-111">Visszaállíthatja az Azure-halom biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="f2b77-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="f2b77-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2b77-112">PARAMETERS</span></span>

### <span data-ttu-id="f2b77-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2b77-113">-AsJob</span></span>
<span data-ttu-id="f2b77-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="f2b77-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b77-115">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="f2b77-115">-DecryptionCertPassword</span></span>
<span data-ttu-id="f2b77-116">A visszafejtési tanúsítvány jelszava.</span><span class="sxs-lookup"><span data-stu-id="f2b77-116">Password of the decryption cert.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b77-117">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="f2b77-117">-DecryptionCertPath</span></span>
<span data-ttu-id="f2b77-118">A visszafejtési tanúsítvány fájljának elérési útja titkos kulccsal (. pfx)</span><span class="sxs-lookup"><span data-stu-id="f2b77-118">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b77-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f2b77-119">-Force</span></span>
<span data-ttu-id="f2b77-120">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f2b77-120">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b77-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="f2b77-121">-Location</span></span>
<span data-ttu-id="f2b77-122">A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="f2b77-122">Name of location to backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b77-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f2b77-123">-Name</span></span>
<span data-ttu-id="f2b77-124">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="f2b77-124">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b77-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2b77-125">-ResourceGroupName</span></span>
<span data-ttu-id="f2b77-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f2b77-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b77-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2b77-127">-ResourceId</span></span>
<span data-ttu-id="f2b77-128">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f2b77-128">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2b77-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f2b77-129">-Confirm</span></span>
<span data-ttu-id="f2b77-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f2b77-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2b77-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2b77-131">-WhatIf</span></span>
<span data-ttu-id="f2b77-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f2b77-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2b77-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f2b77-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2b77-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b77-134">CommonParameters</span></span>
<span data-ttu-id="f2b77-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2b77-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b77-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2b77-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b77-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2b77-137">INPUTS</span></span>

## <span data-ttu-id="f2b77-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2b77-138">OUTPUTS</span></span>

## <span data-ttu-id="f2b77-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2b77-139">NOTES</span></span>

## <span data-ttu-id="f2b77-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2b77-140">RELATED LINKS</span></span>
