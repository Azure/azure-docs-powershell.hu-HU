---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 14e1dd0b897ce5f5c9557ed5aa72c3f63a6514f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679453"
---
# <span data-ttu-id="d4afb-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d4afb-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="d4afb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4afb-102">SYNOPSIS</span></span>
<span data-ttu-id="d4afb-103">Az adattó-tárolóban lévő fájl vagy mappa HOZZÁFÉRÉSének a bejegyzését távolítja el.</span><span class="sxs-lookup"><span data-stu-id="d4afb-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4afb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4afb-104">SYNTAX</span></span>

### <span data-ttu-id="d4afb-105">ACL-Bejegyzések eltávolítása az ACL-objektummal (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4afb-105">Remove ACL Entries using ACL object (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4afb-106">Adott ACE eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d4afb-106">Remove specific ACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4afb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4afb-107">DESCRIPTION</span></span>
<span data-ttu-id="d4afb-108">A **Remove-AzureRmDataLakeStoreItemAclEntry** parancsmag az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájában található bejegyzés (ACE) eltávolítását távolítja el.</span><span class="sxs-lookup"><span data-stu-id="d4afb-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d4afb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d4afb-109">EXAMPLES</span></span>

### <span data-ttu-id="d4afb-110">Példa 1: felhasználó bejegyzésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d4afb-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="d4afb-111">Ez a parancs eltávolítja a felhasználó ACE for Patti Fuller-t az ContosoADL-fiókból.</span><span class="sxs-lookup"><span data-stu-id="d4afb-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

## <span data-ttu-id="d4afb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4afb-112">PARAMETERS</span></span>

### <span data-ttu-id="d4afb-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="d4afb-113">-Account</span></span>
<span data-ttu-id="d4afb-114">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4afb-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4afb-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="d4afb-115">-AceType</span></span>
<span data-ttu-id="d4afb-116">Az eltávolítandó ACE típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4afb-116">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="d4afb-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d4afb-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4afb-118">Felhasználó</span><span class="sxs-lookup"><span data-stu-id="d4afb-118">User</span></span>
- <span data-ttu-id="d4afb-119">Csoport</span><span class="sxs-lookup"><span data-stu-id="d4afb-119">Group</span></span>
- <span data-ttu-id="d4afb-120">Maszk</span><span class="sxs-lookup"><span data-stu-id="d4afb-120">Mask</span></span>
- <span data-ttu-id="d4afb-121">Más</span><span class="sxs-lookup"><span data-stu-id="d4afb-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Remove specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4afb-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="d4afb-122">-Acl</span></span>
<span data-ttu-id="d4afb-123">Megadja az eltávolítandó bejegyzéseket tartalmazó ACL-objektumot.</span><span class="sxs-lookup"><span data-stu-id="d4afb-123">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Remove ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4afb-124">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="d4afb-124">-Default</span></span>
<span data-ttu-id="d4afb-125">Azt jelzi, hogy ez a művelet eltávolítja az alapértelmezett ÁSZT a megadott ACL-ből.</span><span class="sxs-lookup"><span data-stu-id="d4afb-125">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4afb-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d4afb-126">-Id</span></span>
<span data-ttu-id="d4afb-127">Annak az objektumnak az AZONOSÍTÓját adja meg a AzureActive, amelyből egy ÁSZT el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="d4afb-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4afb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4afb-128">-PassThru</span></span>
<span data-ttu-id="d4afb-129">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d4afb-129">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4afb-130">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="d4afb-130">-Path</span></span>
<span data-ttu-id="d4afb-131">Itt adhatja meg az adattó-tároló elérési útját annak az elemnek az elérési útjával, amelyből el szeretné távolítani az ÁSZT (/) a gyökérkönyvtártól kezdve.</span><span class="sxs-lookup"><span data-stu-id="d4afb-131">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4afb-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4afb-132">-Confirm</span></span>
<span data-ttu-id="d4afb-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4afb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4afb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4afb-134">-WhatIf</span></span>
<span data-ttu-id="d4afb-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4afb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4afb-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4afb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4afb-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4afb-137">-DefaultProfile</span></span>
<span data-ttu-id="d4afb-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4afb-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4afb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4afb-139">CommonParameters</span></span>
<span data-ttu-id="d4afb-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4afb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4afb-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4afb-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4afb-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4afb-142">INPUTS</span></span>

### <span data-ttu-id="d4afb-143">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="d4afb-143">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="d4afb-144">Az "ACL" paraméter elfogadja a "DataLakeStoreItemAce []" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d4afb-144">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="d4afb-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4afb-145">OUTPUTS</span></span>

### <span data-ttu-id="d4afb-146">bool</span><span class="sxs-lookup"><span data-stu-id="d4afb-146">bool</span></span>
<span data-ttu-id="d4afb-147">Ha a PassThru meg van adva, akkor a sikeres befejezéshez az igaz értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d4afb-147">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="d4afb-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4afb-148">NOTES</span></span>

## <span data-ttu-id="d4afb-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4afb-149">RELATED LINKS</span></span>

[<span data-ttu-id="d4afb-150">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d4afb-150">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


