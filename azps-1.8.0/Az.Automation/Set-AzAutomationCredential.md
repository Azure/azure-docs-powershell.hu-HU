---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: 7b41b5eaaf0fae38b8cb4e9043b83889e516f93b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671506"
---
# <span data-ttu-id="67743-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="67743-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="67743-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67743-102">SYNOPSIS</span></span>
<span data-ttu-id="67743-103">Automatizálási hitelesítő adatok módosítása</span><span class="sxs-lookup"><span data-stu-id="67743-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="67743-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67743-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67743-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="67743-105">DESCRIPTION</span></span>
<span data-ttu-id="67743-106">A **set-AzAutomationCredential** parancsmag **PSCredential** -objektumként módosítja a hitelesítő adatokat az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="67743-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="67743-107">Példák</span><span class="sxs-lookup"><span data-stu-id="67743-107">EXAMPLES</span></span>

### <span data-ttu-id="67743-108">Példa 1: hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="67743-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="67743-109">Az első parancs a felhasználónevet hozzárendeli a $User változóhoz.</span><span class="sxs-lookup"><span data-stu-id="67743-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="67743-110">A második parancs az egyszerű szöveges jelszót egy biztonságos karakterláncba konvertálja a ConvertTo-SecureString parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="67743-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="67743-111">A parancs az objektumot a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="67743-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="67743-112">A harmadik parancs a hitelesítő adatokat $User és a $Password alapján hozza létre, majd a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="67743-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="67743-113">A végleges parancs módosítja a ContosoCredential nevű automatizálási hitelesítő adatokat, hogy a hitelesítő adatokat használja a $Credentialban.</span><span class="sxs-lookup"><span data-stu-id="67743-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="67743-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67743-114">PARAMETERS</span></span>

### <span data-ttu-id="67743-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="67743-115">-AutomationAccountName</span></span>
<span data-ttu-id="67743-116">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag módosítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="67743-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67743-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67743-117">-DefaultProfile</span></span>
<span data-ttu-id="67743-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="67743-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67743-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="67743-119">-Description</span></span>
<span data-ttu-id="67743-120">A parancsmag által módosított hitelesítő adatok leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="67743-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67743-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="67743-121">-Name</span></span>
<span data-ttu-id="67743-122">Annak a hitelesítő adatoknak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="67743-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67743-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67743-123">-ResourceGroupName</span></span>
<span data-ttu-id="67743-124">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez ez a parancsmag módosítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="67743-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="67743-125">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="67743-125">-Value</span></span>
<span data-ttu-id="67743-126">A hitelesítő adatokat **PSCredential** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="67743-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67743-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67743-127">CommonParameters</span></span>
<span data-ttu-id="67743-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67743-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67743-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67743-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67743-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67743-130">INPUTS</span></span>

### <span data-ttu-id="67743-131">System. String</span><span class="sxs-lookup"><span data-stu-id="67743-131">System.String</span></span>

### <span data-ttu-id="67743-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="67743-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="67743-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67743-133">OUTPUTS</span></span>

### <span data-ttu-id="67743-134">Microsoft. Azure. Command. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="67743-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="67743-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67743-135">NOTES</span></span>

## <span data-ttu-id="67743-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67743-136">RELATED LINKS</span></span>

[<span data-ttu-id="67743-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="67743-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="67743-138">Új – AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="67743-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="67743-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="67743-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


